---
UID: NS:mprapi.RAS_UPDATE_CONNECTION_
title: RAS_UPDATE_CONNECTION_
author: windows-sdk-content
description: Used to update an active RAS connection.
old-location: rras\ras_update_connection.htm
tech.root: rras
ms.assetid: bfa35f1c-e9f5-43f1-ad2d-d54f4675cff8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PRAS_UPDATE_CONNECTION, PRAS_UPDATE_CONNECTION, PRAS_UPDATE_CONNECTION structure pointer [RAS], RAS_UPDATE_CONNECTION, RAS_UPDATE_CONNECTION structure [RAS], RAS_UPDATE_CONNECTION_, mprapi/PRAS_UPDATE_CONNECTION, mprapi/RAS_UPDATE_CONNECTION, rras.ras_update_connection"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - RAS_UPDATE_CONNECTION
product: Windows
targetos: Windows
req.typenames: RAS_UPDATE_CONNECTION, *PRAS_UPDATE_CONNECTION
req.redist: 
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
 

 

