---
UID: NE:d3d11.D3D11_VPOV_DIMENSION
title: D3D11_VPOV_DIMENSION
author: windows-sdk-content
description: Specifies how to access a resource that is used in a video processor output view.
old-location: mf\d3d11_vpov_dimension.htm
old-project: medfound
ms.assetid: EB334FA2-B174-45B2-8087-AAB72BB41795
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: D3D11_VPOV_DIMENSION, D3D11_VPOV_DIMENSION enumeration [Media Foundation], D3D11_VPOV_DIMENSION_TEXTURE2D, D3D11_VPOV_DIMENSION_TEXTURE2DARRAY, D3D11_VPOV_DIMENSION_UNKNOWN, d3d11/D3D11_VPOV_DIMENSION, d3d11/D3D11_VPOV_DIMENSION_TEXTURE2D, d3d11/D3D11_VPOV_DIMENSION_TEXTURE2DARRAY, d3d11/D3D11_VPOV_DIMENSION_UNKNOWN, mf.d3d11_vpov_dimension
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
req.idl: D3d11.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VPOV_DIMENSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VPOV_DIMENSION enumeration


## -description


Specifies how to access a resource that is used in a video processor output view.


## -enum-fields




### -field D3D11_VPOV_DIMENSION_UNKNOWN

Not a valid value.


### -field D3D11_VPOV_DIMENSION_TEXTURE2D

The resource will be accessed as a 2D texture.


### -field D3D11_VPOV_DIMENSION_TEXTURE2DARRAY

The resource will be accessed as an array of 2D textures.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/8E0D44C1-220C-4E70-8A60-591AEBC16A2B">D3D11_VIDEO_PROCESSOR_OUTPUT_VIEW_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>



<a href="https://msdn.microsoft.com/EC7AFE44-877C-4FB0-9E61-FCD504A334D3">ID3D11VideoDevice::CreateVideoProcessorOutputView</a>
 

 

