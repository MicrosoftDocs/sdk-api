---
UID: NS:gdipluseffects.BrightnessContrastParams
title: BrightnessContrastParams
author: windows-sdk-content
description: A BrightnessContrastParams structure contains members that specify the nature of a brightness or contrast adjustment.
old-location: gdiplus\_gdiplus_STRUC_BrightnessContrastParams.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\brightnesscontrastparams.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: BrightnessContrastParams, BrightnessContrastParams structure [GDI+], _gdiplus_STRUC_BrightnessContrastParams, gdiplus._gdiplus_STRUC_BrightnessContrastParams, gdipluseffects/BrightnessContrastParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: gdipluseffects.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluseffects.h
api_name:
 - BrightnessContrastParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# BrightnessContrastParams structure


## -description


A <b>BrightnessContrastParams</b> structure contains members that specify the nature of a brightness or contrast adjustment.

You can change the brightness or contrast (or both) of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>BrightnessContrastParams</b> structure.</li>
<li>Pass the address of the <b>BrightnessContrastParams</b> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536278(v=VS.85).aspx">BrightnessContrast::SetParameters</a> method of a <a href="https://msdn.microsoft.com/en-us/library/ms534423(v=VS.85).aspx">BrightnessContrast</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534423(v=VS.85).aspx">BrightnessContrast</a> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field brightnessLevel

Type: <b>INT</b>

Integer in the range -255 through 255 that specifies the brightness level. If the value is 0, the brightness remains the same. As the value moves from 0 to 255, the brightness of the image increases. As the value moves from 0 to -255, the brightness of the image decreases.


### -field contrastLevel

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies the contrast level. If the value is 0, the contrast remains the same. As the value moves from 0 to 100, the contrast of the image increases. As the value moves from 0 to -100, the contrast of the image decreases.

