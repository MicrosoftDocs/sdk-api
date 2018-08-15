---
UID: NE:d3d11.D3D11_VPIV_DIMENSION
title: D3D11_VPIV_DIMENSION
author: windows-sdk-content
description: Specifies how to access a resource that is used in a video processor input view.
old-location: mf\d3d11_vpiv_dimension.htm
old-project: medfound
ms.assetid: 65003974-F86E-4604-BA8D-262CA2674D53
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_VPIV_DIMENSION, D3D11_VPIV_DIMENSION enumeration [Media Foundation], D3D11_VPIV_DIMENSION_TEXTURE2D, D3D11_VPIV_DIMENSION_UNKNOWN, d3d11/D3D11_VPIV_DIMENSION, d3d11/D3D11_VPIV_DIMENSION_TEXTURE2D, d3d11/D3D11_VPIV_DIMENSION_UNKNOWN, mf.d3d11_vpiv_dimension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_VPIV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VPIV_DIMENSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VPIV_DIMENSION enumeration


## -description


Specifies how to access a resource that is used in a video processor input view.


## -enum-fields




### -field D3D11_VPIV_DIMENSION_UNKNOWN

Not a valid value.


### -field D3D11_VPIV_DIMENSION_TEXTURE2D

The resource will be accessed as a 2D texture.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/69EDF918-355A-4277-9F7E-C08CF65E5418">D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>



<a href="https://msdn.microsoft.com/3245D2AF-74A1-4068-A0BC-577FD42B353E">ID3D11VideoDevice::CreateVideoProcessorInputView</a>
 

 

