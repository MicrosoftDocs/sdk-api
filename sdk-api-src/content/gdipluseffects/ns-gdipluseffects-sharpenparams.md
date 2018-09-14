---
UID: NS:gdipluseffects.SharpenParams
title: SharpenParams
author: windows-sdk-content
description: The SharpenParams structure contains members that specify the nature of a sharpening adjustment to a bitmap.
old-location: gdiplus\_gdiplus_STRUC_SharpenParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\sharpenparams.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: SharpenParams, SharpenParams structure [GDI+], _gdiplus_STRUC_SharpenParams, gdiplus._gdiplus_STRUC_SharpenParams, gdipluseffects/SharpenParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - SharpenParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# SharpenParams structure


## -description


The <b>SharpenParams</b> structure contains members that specify the nature of a sharpening adjustment to a bitmap.

You can adjust the sharpness of a bitmap by following these steps. 
<ol>
<li>Create and initialize a <b>SharpenParams</b> structure.</li>
<li>Pass the address of the <b>SharpenParams</b> structure to the <a href="https://msdn.microsoft.com/279fee59-6fcf-4a9d-b16e-e6de6b5977c1">Sharpen::SetParameters</a> method of a <a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field radius

Type: <b>REAL</b>

Real number that specifies the sharpening radius (the radius of the convolution kernel) in pixels. The radius must be in the range 0 through 255. As the radius increases, more surrounding pixels are involved in calculating the new value of a given pixel.


### -field amount

Type: <b>REAL</b>

Real number in the range 0 through 100 that specifies the amount of sharpening to be applied. A value of 0 specifies no sharpening. As the value of <b>amount</b> increases, the sharpness increases.

