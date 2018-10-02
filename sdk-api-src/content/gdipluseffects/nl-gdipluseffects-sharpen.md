---
UID: NL:gdipluseffects.Sharpen
title: Sharpen
author: windows-sdk-content
description: The Sharpen class enables you to adjust the sharpness of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_Sharpen_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sharpen.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
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


The <b>Sharpen</b> class enables you to adjust the sharpness of a bitmap. Pass the address of a <b>Sharpen</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the nature of the sharpening adjustment, pass the address of a <a href="https://msdn.microsoft.com/9a3dd5ec-789b-4191-a680-6d85c12ab97b">SharpenParams</a> structure to the <a href="https://msdn.microsoft.com/279fee59-6fcf-4a9d-b16e-e6de6b5977c1">Sharpen::SetParameters</a> method of a <b>Sharpen</b> object.

