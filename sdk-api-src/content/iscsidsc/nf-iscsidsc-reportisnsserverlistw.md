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

# ReportISNSServerListW function


## -description


The <b>ReportIsnsServerList</b> function retrieves the list of Internet Storage Name Service (iSNS) servers that the iSCSI initiator service queries for discovered targets.



## -parameters




### -param BufferSizeInChar [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 
If the operation succeeds, this location receives the size, represented by a number of  elements, that corresponds to the number of retrieved iSNS servrs.


### -param Buffer [out]

The buffer that holds the list of iSNS servers on output. Each server name is <b>null</b> terminated, except for the last server name, which is double <b>null</b> terminated. 



## -returns



Returns ERROR_SUCCESS if the operation succeeds and ERROR_INSUFFICIENT_BUFFER if the buffer is too small to hold the output data. 

Otherwise, <b>ReportIsnsServerList</b> returns the appropriate Win32 or iSCSI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550125">AddIsnsServer</a>



<a href="https://msdn.microsoft.com/c954126a-6bad-49cf-889e-81746fe175a4">RefreshIsnsServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563978">RemoveIsnsServer</a>
 

 

