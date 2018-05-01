---
UID: NS:ntddpar._PAR_SET_INFORMATION
title: "_PAR_SET_INFORMATION"
author: windows-driver-content
description: The PAR_SET_INFORMATION structure specifies the initial operating status of a parallel port.
old-location: parports\par_set_information.htm
old-project: parports
ms.assetid: 05e889b1-4b18-4122-9332-69778017e15c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PPAR_SET_INFORMATION, PAR_SET_INFORMATION, PAR_SET_INFORMATION structure [Parallel Ports], PPAR_SET_INFORMATION, PPAR_SET_INFORMATION structure pointer [Parallel Ports], _PAR_SET_INFORMATION, cisspd_8390a7d0-a4b2-4970-94f8-fd270f2d8256.xml, ntddpar/PAR_SET_INFORMATION, ntddpar/PPAR_SET_INFORMATION, parports.par_set_information"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddpar.h
req.include-header: Ntddpar.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PAR_SET_INFORMATION, *PPAR_SET_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddpar.h
api_name:
-	PAR_SET_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _PAR_SET_INFORMATION structure


## -description


The PAR_SET_INFORMATION structure specifies the initial operating status of a parallel port.


## -struct-fields




### -field Init

Specifies the operating status of the parallel port. Must be set to PARALLEL_INIT.


## -remarks



This structure is used with an <a href="https://msdn.microsoft.com/library/windows/hardware/ff544103">IOCTL_PAR_SET_INFORMATION</a> request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544086">IOCTL_PAR_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544103">IOCTL_PAR_SET_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544353">PAR_QUERY_INFORMATION</a>
 

 

