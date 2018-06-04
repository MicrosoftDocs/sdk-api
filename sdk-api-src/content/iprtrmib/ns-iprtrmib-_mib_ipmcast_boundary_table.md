---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MIB_IPMCAST_BOUNDARY_TABLE structure


## -description


The <b>MIB_IPMCAST_BOUNDARY_TABLE</b> structure contains a list of  a router's scoped IPv4 multicast address boundaries.


## -struct-fields




### -field dwNumEntries

The number of <a href="https://msdn.microsoft.com/a3d900be-14c9-4ad9-bc2e-382849a6d1c6">MIB_IPMCAST_BOUNDARY</a> structures listed in <b>table[]</b>.


### -field table

An array of <a href="https://msdn.microsoft.com/a3d900be-14c9-4ad9-bc2e-382849a6d1c6">MIB_IPMCAST_BOUNDARY</a> structures which collectively define the set of scoped IPv4 multicast address boundaries on a router.


## -remarks



This structure does not have a fixed size. Use the <b>SIZEOF_BOUNDARY_TABLE(X)</b> macro to determine the size of this structure. This macro is defined in the <i>Iprtrmib.h</i> header file.

Note that the <i>Iprtrmib.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Iprtrmib.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/a3d900be-14c9-4ad9-bc2e-382849a6d1c6">MIB_IPMCAST_BOUNDARY</a>
 

 

