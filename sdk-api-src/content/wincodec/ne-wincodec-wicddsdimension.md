---
UID: NE:wincodec.WICDdsDimension
title: WICDdsDimension
author: windows-driver-content
description: Specifies the dimension type of the data contained in DDS image.
old-location: wic\wicddsdimension.htm
old-project: wic
ms.assetid: 76CEBFD7-EE7D-48C4-9F88-9AD82C9FED55
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WICDdsDimension, WICDdsDimension enumeration [Windows Imaging Component], WICDdsTexture1D, WICDdsTexture2D, WICDdsTexture3D, WICDdsTextureCube, wic.wicddsdimension, wincodec/WICDdsDimension, wincodec/WICDdsTexture1D, wincodec/WICDdsTexture2D, wincodec/WICDdsTexture3D, wincodec/WICDdsTextureCube
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICDdsDimension
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincodec.h
api_name:
-	WICDdsDimension
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICDdsDimension enumeration


## -description


Specifies the dimension type of the data contained in DDS image.


## -enum-fields




### -field WICDdsTexture1D

DDS image contains a 1-dimensional texture .  


### -field WICDdsTexture2D

DDS image contains a 2-dimensional texture .  


### -field WICDdsTexture3D

DDS image contains a 3-dimensional texture .  


### -field WICDdsTextureCube

The DDS image contains a cube texture represented as an array of 6 faces.  


### -field WICDDSTEXTURE_FORCE_DWORD




## -remarks



Both <b>WICDdsTexture2d</b> and <b>WICDdsTextureCube</b> correspond to <a href="https://msdn.microsoft.com/56f138a2-9f2b-4f3b-8619-d9f394704b8a">D3D11_RESOURCE_DIMENSION_TEXTURE2D</a>. When using <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a>, they are distinguished by the flag <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_TEXTURECUBE</a> in the structure <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a>.




## -see-also




<a href="https://msdn.microsoft.com/D4EE39D6-54DC-450D-A430-2996D349BEC6">IWICDdsDecoder::GetParameters</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

