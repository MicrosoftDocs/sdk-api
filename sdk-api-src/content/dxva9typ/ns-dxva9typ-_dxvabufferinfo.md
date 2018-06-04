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

# _DXVABufferInfo structure


## -description


Specifies a buffer for the 
        <a href="https://msdn.microsoft.com/cb87a087-ca53-470e-ab46-f4022cfd7869">IDirect3DDXVADevice9::Execute</a>  method.


## -struct-fields




### -field pCompSurface

A pointer to the <b>IDirect3DSurface9</b> interface.


### -field DataOffset

The offset of the relevant data from the beginning of the buffer, in bytes.


### -field DataSize

The size of the relevant data in the buffer, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a>
 

 

