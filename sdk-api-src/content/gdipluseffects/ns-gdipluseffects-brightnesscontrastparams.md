---
UID: NS:gdipluseffects.BrightnessContrastParams
title: BrightnessContrastParams
author: windows-sdk-content
description: A BrightnessContrastParams structure contains members that specify the nature of a brightness or contrast adjustment.
old-location: gdiplus\_gdiplus_STRUC_BrightnessContrastParams.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\brightnesscontrastparams.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BrightnessContrastParams, BrightnessContrastParams structure [GDI+], _gdiplus_STRUC_BrightnessContrastParams, gdiplus._gdiplus_STRUC_BrightnessContrastParams, gdipluseffects/BrightnessContrastParams
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - BrightnessContrastParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# BrightnessContrastParams structure


## -description


A <b>BrightnessContrastParams</b> structure contains members that specify the nature of a brightness or contrast adjustment.

You can change the brightness or contrast (or both) of a bitmap by following these steps.
<ol>
<li>Create and initialize a <b>BrightnessContrastParams</b> structure.</li>
<li>Pass the address of the <b>BrightnessContrastParams</b> structure to the <a href="https://msdn.microsoft.com/ca9e5978-75ff-4e06-9597-0e706db19259">BrightnessContrast::SetParameters</a> method of a <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object.</li>
<li>Pass the address of the <a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.</li>
</ol>

## -struct-fields




### -field brightnessLevel

Type: <b>INT</b>

Integer in the range -255 through 255 that specifies the brightness level. If the value is 0, the brightness remains the same. As the value moves from 0 to 255, the brightness of the image increases. As the value moves from 0 to -255, the brightness of the image decreases.


### -field contrastLevel

Type: <b>INT</b>

Integer in the range -100 through 100 that specifies the contrast level. If the value is 0, the contrast remains the same. As the value moves from 0 to 100, the contrast of the image increases. As the value moves from 0 to -100, the contrast of the image decreases.

