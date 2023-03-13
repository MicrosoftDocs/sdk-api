---
UID: NE:wincodec.WICGifGraphicControlExtensionProperties
title: WICGifGraphicControlExtensionProperties (wincodec.h)
description: Specifies the graphic control extension metadata properties that define the transitions between each frame animation for Graphics Interchange Format (GIF) images.
helpviewer_keywords: ["WICGifGraphicControlExtensionDelay","WICGifGraphicControlExtensionDisposal","WICGifGraphicControlExtensionProperties","WICGifGraphicControlExtensionProperties enumeration [Windows Imaging Component]","WICGifGraphicControlExtensionTransparencyFlag","WICGifGraphicControlExtensionTransparentColorIndex","WICGifGraphicControlExtensionUserInputFlag","_wic_codec_wicgifgraphiccontrolextensionproperties","wic._wic_codec_wicgifgraphiccontrolextensionproperties","wincodec/WICGifGraphicControlExtensionDelay","wincodec/WICGifGraphicControlExtensionDisposal","wincodec/WICGifGraphicControlExtensionProperties","wincodec/WICGifGraphicControlExtensionTransparencyFlag","wincodec/WICGifGraphicControlExtensionTransparentColorIndex","wincodec/WICGifGraphicControlExtensionUserInputFlag"]
old-location: wic\_wic_codec_wicgifgraphiccontrolextensionproperties.htm
tech.root: wic
ms.assetid: 32fbf62d-0479-4ead-8246-6c757467ccaa
ms.date: 12/05/2018
ms.keywords: WICGifGraphicControlExtensionDelay, WICGifGraphicControlExtensionDisposal, WICGifGraphicControlExtensionProperties, WICGifGraphicControlExtensionProperties enumeration [Windows Imaging Component], WICGifGraphicControlExtensionTransparencyFlag, WICGifGraphicControlExtensionTransparentColorIndex, WICGifGraphicControlExtensionUserInputFlag, _wic_codec_wicgifgraphiccontrolextensionproperties, wic._wic_codec_wicgifgraphiccontrolextensionproperties, wincodec/WICGifGraphicControlExtensionDelay, wincodec/WICGifGraphicControlExtensionDisposal, wincodec/WICGifGraphicControlExtensionProperties, wincodec/WICGifGraphicControlExtensionTransparencyFlag, wincodec/WICGifGraphicControlExtensionTransparentColorIndex, wincodec/WICGifGraphicControlExtensionUserInputFlag
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
req.typenames: WICGifGraphicControlExtensionProperties
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICGifGraphicControlExtensionProperties
 - wincodec/WICGifGraphicControlExtensionProperties
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
 - WICGifGraphicControlExtensionProperties
---

# WICGifGraphicControlExtensionProperties enumeration


## -description

Specifies the graphic control extension metadata properties that define the transitions between each frame animation for Graphics Interchange Format (GIF) images.

## -enum-fields

### -field WICGifGraphicControlExtensionDisposal:0x1

[VT_UI1] Indicates  the disposal requirements. 0 - no disposal, 1 - do not dispose, 2 - restore to background color, 3 - restore to previous.

### -field WICGifGraphicControlExtensionUserInputFlag:0x2

[VT_BOOL] Indicates the user input flag. <b>TRUE</b> if user input should advance to the next frame; otherwise, <b>FALSE</b>.

### -field WICGifGraphicControlExtensionTransparencyFlag:0x3

[VT_BOOL] Indicates the transparency flag. <b>TRUE</b> if a transparent color in is in the color table for this frame; otherwise, <b>FALSE</b>.

### -field WICGifGraphicControlExtensionDelay:0x4

[VT_UI2] Indicates  how long to display the next frame before advancing to the next frame, in units of 1/100th of a second.

### -field WICGifGraphicControlExtensionTransparentColorIndex:0x5

[VT_UI1] Indicates which color in the palette should be treated as transparent.

### -field WICGifGraphicControlExtensionProperties_FORCE_DWORD:0x7fffffff

