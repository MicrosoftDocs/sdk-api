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

# IDirect3DIndexBuffer9::GetDesc


## -description


Retrieves a description of the index buffer resource.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/5d45213e-b3c0-4eb7-a4f9-8d8730eb3899">D3DINDEXBUFFER_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/5d45213e-b3c0-4eb7-a4f9-8d8730eb3899">D3DINDEXBUFFER_DESC</a> structure, describing the returned index buffer. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -see-also




<a href="https://msdn.microsoft.com/df1b7898-6c6b-410b-8ff9-e56625584fdc">IDirect3DIndexBuffer9</a>



<a href="https://msdn.microsoft.com/baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784">Index Buffers (Direct3D 9)</a>
 

 

