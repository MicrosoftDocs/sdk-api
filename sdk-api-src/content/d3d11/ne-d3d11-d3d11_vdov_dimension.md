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

# D3D11_VDOV_DIMENSION enumeration


## -description


Specifies how to access a resource that is used in a video decoding output view.


## -enum-fields




### -field D3D11_VDOV_DIMENSION_UNKNOWN

Not a valid value.


### -field D3D11_VDOV_DIMENSION_TEXTURE2D

The resource will be accessed as a 2D texture.



## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/0A0C29C5-C3A3-43E7-86DA-1849AC276060">D3D11_VIDEO_DECODER_OUTPUT_VIEW_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>



<a href="https://msdn.microsoft.com/8A3D72CF-B641-4219-8C88-FCE5231CF2F6">ID3D11VideoDevice::CreateVideoDecoderOutputView</a>
 

 

