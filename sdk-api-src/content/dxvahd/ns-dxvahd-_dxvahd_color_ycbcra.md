---
UID: NS:dxvahd._DXVAHD_COLOR_YCbCrA
title: "_DXVAHD_COLOR_YCbCrA"
author: windows-sdk-content
description: Specifies a YCbCr color value.
old-location: mf\dxvahd_color_ycbcra.htm
tech.root: medfound
ms.assetid: 3e37daf1-5529-4042-ab6e-89a7f77d5e15
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DXVAHD_COLOR_YCbCrA, DXVAHD_COLOR_YCbCrA structure [Media Foundation], _DXVAHD_COLOR_YCbCrA, dxvahd/DXVAHD_COLOR_YCbCrA, mf.dxvahd_color_ycbcra
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - dxvahd.h
api_name:
 - DXVAHD_COLOR_YCbCrA
product: Windows
targetos: Windows
req.typenames: DXVAHD_COLOR_YCbCrA
req.redist: 
---

# _DXVAHD_COLOR_YCbCrA structure


## -description


Specifies a YCbCr color value.


## -struct-fields




### -field Y

The Y (luma) value.


### -field Cb

The Cb chroma value.


### -field Cr

The Cr chroma value.


### -field A

The alpha value. Values range from 0 (transparent) to 1 (opaque).



## -remarks



Values have a nominal range of [0...1]. Given a format with  <i>n</i> bits per channel, the value of each color component is calculated as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

For example, for 8-bit YUV formats, <code>val = BYTE(f * 255.0)</code>.

Reference black is (0.0625, 0.5, 0.5), which corresponds to (16, 128, 128) in an 8-bit representation.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

