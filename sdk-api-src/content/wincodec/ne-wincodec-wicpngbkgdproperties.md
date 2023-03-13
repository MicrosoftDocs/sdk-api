---
UID: NE:wincodec.WICPngBkgdProperties
title: WICPngBkgdProperties (wincodec.h)
description: Specifies the Portable Network Graphics (PNG) background (bKGD) chunk metadata properties.
helpviewer_keywords: ["WICPngBkgdBackgroundColor","WICPngBkgdProperties","WICPngBkgdProperties enumeration [Windows Imaging Component]","_wic_codec_wicpngbkgdproperties","wic._wic_codec_wicpngbkgdproperties","wincodec/WICPngBkgdBackgroundColor","wincodec/WICPngBkgdProperties"]
old-location: wic\_wic_codec_wicpngbkgdproperties.htm
tech.root: wic
ms.assetid: 979f6a91-79a2-4eba-8957-e2908636cdc5
ms.date: 12/05/2018
ms.keywords: WICPngBkgdBackgroundColor, WICPngBkgdProperties, WICPngBkgdProperties enumeration [Windows Imaging Component], _wic_codec_wicpngbkgdproperties, wic._wic_codec_wicpngbkgdproperties, wincodec/WICPngBkgdBackgroundColor, wincodec/WICPngBkgdProperties
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
req.typenames: WICPngBkgdProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICPngBkgdProperties
 - wincodec/WICPngBkgdProperties
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
 - WICPngBkgdProperties
---

# WICPngBkgdProperties enumeration


## -description

Specifies the Portable Network Graphics (PNG) background (bKGD) chunk metadata properties.

## -enum-fields

### -field WICPngBkgdBackgroundColor:0x1

Indicates the background color. There are three possible types, depending on the image's pixel format.





#### VT_UI1

Specifies the index of the background color in an image with an indexed pixel format.



#### VT_UI2

Specifies the background color in a grayscale image.



#### VT_VECTOR|VT_UI2

Specifies the background color in an RGB image as three USHORT values: {0x<i>RRRR</i>, 0x<i>GGGG</i>, 0x<i>BBBB</i>}.

### -field WICPngBkgdProperties_FORCE_DWORD:0x7fffffff

