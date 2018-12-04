---
UID: NL:gdipluseffects.BrightnessContrast
title: BrightnessContrast
author: windows-sdk-content
description: The BrightnessContrast class enables you to change the brightness and contrast of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrast.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: BrightnessContrast, BrightnessContrast class [GDI+], BrightnessContrast class [GDI+],described, _gdiplus_CLASS_BrightnessContrast_Class, gdiplus._gdiplus_CLASS_BrightnessContrast_Class, gdipluseffects/BrightnessContrast
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdipluseffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - BrightnessContrast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BrightnessContrast class


## -description


The <b>BrightnessContrast</b> class enables you to change the brightness and contrast of a bitmap. Pass the address of a <b>BrightnessContrast</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the brightness and contrast levels, pass a <a href="https://msdn.microsoft.com/b5271911-7759-4e87-af25-7d9a9d9c653e">BrightnessContrastParams</a> structure to the <a href="https://msdn.microsoft.com/ca9e5978-75ff-4e06-9597-0e706db19259">BrightnessContrast::SetParameters</a> method of a <b>BrightnessContrast</b> object.

