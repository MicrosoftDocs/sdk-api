---
UID: NS:gdipluseffects.BlurParams
title: BlurParams
author: windows-sdk-content
description: A BlurParams structure contains members that specify the nature of a Gaussian blur.
old-location: gdiplus\_gdiplus_STRUC_BlurParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\blurparams.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BlurParams, BlurParams structure [GDI+], _gdiplus_STRUC_BlurParams, gdiplus._gdiplus_STRUC_BlurParams, gdipluseffects/BlurParams
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
 - BlurParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# BlurParams structure


## -description


A <b>BlurParams</b> structure contains members that specify the nature of a Gaussian blur.

 You can apply a Gaussian blur effect to a bitmap by following these steps. 
<ol>
<li>Create and initialize a <b>BlurParams</b> structure.</li>
<li>Pass the address of the <b>BlurParams</b> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536282(v=VS.85).aspx">Blur::SetParameters</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534422(v=VS.85).aspx">Blur</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534422(v=VS.85).aspx">Blur</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field radius

Type: <b>float</b>

Real number that specifies the blur radius (the radius of the Gaussian convolution kernel) in pixels. The radius must be in the range 0 through 255. As the radius increases, the resulting bitmap becomes more blurry. 


### -field expandEdge

Type: <b>BOOL</b>

Boolean value that specifies whether the bitmap expands by an amount equal to the blur radius. If <b>TRUE</b>, the bitmap expands by an amount equal to the radius so that it can have soft edges. If <b>FALSE</b>, the bitmap remains the same size and the soft edges are clipped.


## -remarks



One of the two <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> methods blurs a bitmap in place. That particular <a href="https://msdn.microsoft.com/en-us/library/ms536321(v=VS.85).aspx">Bitmap::ApplyEffect</a> method ignores the <b>expandEdge</b> parameter.
          



