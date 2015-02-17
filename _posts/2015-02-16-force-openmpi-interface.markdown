---
layout: post
title:  "Force OpenMPI to Utilize a Particular Interface"
date:   2015-02-16 20:24:00
categories: 
---

Was fighting error messages that looked like this:

    [n50][[41350,2],0][../../../../../../ompi/mca/btl/tcp/btl_tcp_endpoint.c:638:mca_btl_tcp_endpoint_complete_connect] connect() to 192.168.161.32 failed: No route to host (113)

In R, require OpenMPI to utilize a particular interface.  Add this line before utilizing mpi.spawn.Rslaves(). 

    Sys.setenv(OMPI_MCA_btl_tcp_if_include='eth0')


