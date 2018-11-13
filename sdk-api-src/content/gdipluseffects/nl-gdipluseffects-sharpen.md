---
UID: NL:gdipluseffects.Sharpen
title: Sharpen
author: windows-sdk-content
description: The Sharpen class enables you to adjust the sharpness of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_Sharpen_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sharpen.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Sharpen, Sharpen class [GDI+], Sharpen class [GDI+],described, _gdiplus_CLASS_Sharpen_Class, gdiplus._gdiplus_CLASS_Sharpen_Class, gdipluseffects/Sharpen
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
 - Sharpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Sharpen class


## -description


The <b>Sharpen</b> class enables you to adjust the sharpness of a bitmap. Pass the address of a <b>Sharpen</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the nature of the sharpening adjustment, pass the address of a <a href="https://msdn.microsoft.com/en-us/library/ms534073(v=VS.85).aspx">SharpenParams</a> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms534758(v=VS.85).aspx">Sharpen::SetParameters</a> method of a <b>Sharpen</b> object.

