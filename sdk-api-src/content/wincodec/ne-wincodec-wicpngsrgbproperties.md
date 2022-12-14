---
UID: NE:wincodec.WICPngSrgbProperties
title: WICPngSrgbProperties (wincodec.h)
description: Specifies the Portable Network Graphics (PNG) sRGB chunk metadata properties.
helpviewer_keywords: ["WICPngSrgbProperties","WICPngSrgbProperties enumeration [Windows Imaging Component]","WICPngSrgbRenderingIntent","_wic_codec_wicpngsrgbproperties","wic._wic_codec_wicpngsrgbproperties","wincodec/WICPngSrgbProperties","wincodec/WICPngSrgbRenderingIntent"]
old-location: wic\_wic_codec_wicpngsrgbproperties.htm
tech.root: wic
ms.assetid: ec9bbdb7-9ce2-44bd-bd84-842394ce4c5f
ms.date: 12/05/2018
ms.keywords: WICPngSrgbProperties, WICPngSrgbProperties enumeration [Windows Imaging Component], WICPngSrgbRenderingIntent, _wic_codec_wicpngsrgbproperties, wic._wic_codec_wicpngsrgbproperties, wincodec/WICPngSrgbProperties, wincodec/WICPngSrgbRenderingIntent
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICPngSrgbProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICPngSrgbProperties
 - wincodec/WICPngSrgbProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICPngSrgbProperties
---

# WICPngSrgbProperties enumeration


## -description

Specifies the Portable Network Graphics (PNG) sRGB chunk metadata properties.

## -enum-fields

### -field WICPngSrgbRenderingIntent:0x1

[VT_UI1] Indicates the rendering intent for an sRGB color space image. The rendering intents have the following meaning.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Perceptual</td>
</tr>
<tr>
<td>1</td>
<td>Relative colorimetric</td>
</tr>
<tr>
<td>2</td>
<td>Saturation</td>
</tr>
<tr>
<td>3</td>
<td>Absolute colorimetric</td>
</tr>
</table>

### -field WICPngSrgbProperties_FORCE_DWORD:0x7fffffff

