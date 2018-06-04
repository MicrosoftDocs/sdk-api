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

# D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC structure


## -description


Describes a video processor output view.


## -struct-fields




### -field ViewDimension

The resource type of the view, specified as a member of the <a href="https://msdn.microsoft.com/EB334FA2-B174-45B2-8087-AAB72BB41795">D3D11_VPOV_DIMENSION</a> enumeration.


### -field Texture2D

A <a href="https://msdn.microsoft.com/DFABFB34-2622-4AB7-A87E-7E15F4D20E69">D3D11_TEX2D_VPOV</a> structure that identifies the texture resource for the output view. 

Use this member of the union when <b>ViewDimension</b> equals <b>D3D11_VPOV_DIMENSION_TEXTURE2D</b>.


### -field Texture2DArray

A <a href="https://msdn.microsoft.com/DF059392-3E4B-45D2-A3CD-A0C61C8D628F">D3D11_TEX2D_ARRAY_VPOV</a> structure that identifies the texture array for the output view. 

Use this member of the union when <b>ViewDimension</b> equals <b>D3D11_VPOV_DIMENSION_TEXTURE2DARRAY</b>.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/EC7AFE44-877C-4FB0-9E61-FCD504A334D3">ID3D11VideoDevice::CreateVideoProcessorOutputView</a>
 

 

