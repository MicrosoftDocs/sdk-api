---
UID: NS:dxva9typ._DXVAUncompDataInfo
title: "_DXVAUncompDataInfo"
author: windows-driver-content
description: Specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.
old-location: mf\dxvauncompdatainfo.htm
old-project: medfound
ms.assetid: bd19d9a8-7d69-4aea-9638-84c3f1a1e810
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: DXVAUncompDataInfo, DXVAUncompDataInfo structure [Media Foundation], _DXVAUncompDataInfo, dxva9typ/DXVAUncompDataInfo, mf.dxvauncompdatainfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva9typ.h
api_name:
-	DXVAUncompDataInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAUncompDataInfo structure


## -description


Specifies the dimensions and pixel format of the uncompressed surfaces for DirectX Video Acceleration (DXVA) video decoding.



## -struct-fields




### -field UncompWidth

The width of the uncompressed data, in pixels.




### -field UncompHeight

The height of the uncompressed data, in pixels.


### -field UncompFormat

The pixel format of the uncompressed data, specified as a <b>D3DFORMAT</b> value.


## -see-also




<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/abe3beac-f3f8-413d-8b83-9da3340b19ac">IDirect3DVideoDevice9</a>
 

 

