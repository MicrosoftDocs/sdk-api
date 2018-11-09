---
UID: NE:d3d11.D3D11_VDOV_DIMENSION
title: D3D11_VDOV_DIMENSION
author: windows-sdk-content
description: Specifies how to access a resource that is used in a video decoding output view.
old-location: mf\d3d11_vdov_dimension.htm
tech.root: medfound
ms.assetid: 079460EB-A7D4-4C8C-B7CA-9A6FFB3B0FA8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: D3D11_VDOV_DIMENSION, D3D11_VDOV_DIMENSION enumeration [Media Foundation], D3D11_VDOV_DIMENSION_TEXTURE2D, D3D11_VDOV_DIMENSION_UNKNOWN, d3d11/D3D11_VDOV_DIMENSION, d3d11/D3D11_VDOV_DIMENSION_TEXTURE2D, d3d11/D3D11_VDOV_DIMENSION_UNKNOWN, mf.d3d11_vdov_dimension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - D3D11_VDOV_DIMENSION
product: Windows
targetos: Windows
req.typenames: D3D11_VDOV_DIMENSION
req.redist: 
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
 

 

