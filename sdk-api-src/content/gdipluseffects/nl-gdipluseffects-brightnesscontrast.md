---
UID: NL:gdipluseffects.BrightnessContrast
title: BrightnessContrast
author: windows-sdk-content
description: The BrightnessContrast class enables you to change the brightness and contrast of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_BrightnessContrast_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brightnesscontrast.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: BrightnessContrast, BrightnessContrast class [GDI+], BrightnessContrast class [GDI+],described, _gdiplus_CLASS_BrightnessContrast_Class, gdiplus._gdiplus_CLASS_BrightnessContrast_Class, gdipluseffects/BrightnessContrast
ms.prod: windows
ms.technology: windows-sdk
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


The <b>BrightnessContrast</b> class enables you to change the brightness and contrast of a bitmap. Pass the address of a <b>BrightnessContrast</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the brightness and contrast levels, pass a <a href="https://msdn.microsoft.com/en-us/library/ms534058(v=VS.85).aspx">BrightnessContrastParams</a> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536278(v=VS.85).aspx">BrightnessContrast::SetParameters</a> method of a <b>BrightnessContrast</b> object.

