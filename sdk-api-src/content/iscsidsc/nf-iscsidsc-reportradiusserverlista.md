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

# ReportRadiusServerListA function


## -description


The <b>ReportRadiusServerList</b> function  retrieves the list of Remote Authentication Dail-In Service (RADIUS) servers the iSCSI initiator service uses during authentication.


## -parameters




### -param BufferSizeInChar [in, out]

A <b>ULONG</b> value that specifies the number of list elements contained by the <i>Buffer</i> parameter. 



### -param Buffer [out, optional]

Pointer to a buffer that receives the list of Remote Authentication Dail-In Service (RADIUS) servers on output. Each server name is null terminated, except for the last server name, which is double null-terminated.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation is successful. If the operation fails due to a socket connection error, this function will return a Winsock error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550133">AddRadiusServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564020">RemoveRadiusServer</a>
 

 

