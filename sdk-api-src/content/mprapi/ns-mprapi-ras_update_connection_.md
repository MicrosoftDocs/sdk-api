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

# RAS_UPDATE_CONNECTION_ structure


## -description


The <a href="https://msdn.microsoft.com/eb665afb-2ffd-484b-b7b6-04a92879c98c">RAS_UPDATE_CONNECTION</a> structure is  used to update an active RAS connection.


## -struct-fields




### -field Header

A <a href="https://msdn.microsoft.com/2f4e1ddc-7991-4091-9889-fdd2d75e702f">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <a href="https://msdn.microsoft.com/eb665afb-2ffd-484b-b7b6-04a92879c98c">RAS_UPDATE_CONNECTION</a> structure. 

<div class="alert"><b>Note</b>  The <b>revision</b> member  of  <b>Header</b> must be <b>0x01</b> and <b>type</b> must be <b>MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT</b>.</div>
<div> </div>

### -field dwIfIndex

A value that specifies the new interface index of the Virtual Private Network (VPN) endpoint.


### -field wszLocalEndpointAddress

A null-terminated Unicode string that contains the new IP address of the local computer in the connection. This string is of the form "a.b.c.d".


### -field wszRemoteEndpointAddress

A null-terminated Unicode string that contains the new IP address of the remote computer in the connection. This string is of the form "a.b.d.c".


## -see-also




<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 

