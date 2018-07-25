---
UID: NL:gdipluseffects.Tint
title: Tint
author: windows-sdk-content
description: The Tint class enables you to apply a tint to a bitmap.
old-location: gdiplus\_gdiplus_CLASS_Tint_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tint.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Tint, Tint class [GDI+], Tint class [GDI+],described, _gdiplus_CLASS_Tint_Class, gdiplus._gdiplus_CLASS_Tint_Class, gdipluseffects/Tint
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - Tint
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Tint class


## -description


The <b>Tint</b> class enables you to apply a tint to a bitmap. Pass the address of a <b>Tint</b> object to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. To specify the nature of the tint, pass the address of a <a href="https://msdn.microsoft.com/d2d012d7-1e9e-4aea-a28c-df2d42ca1b69">TintParams</a> structure to the <a href="https://msdn.microsoft.com/f1d19fc2-2912-47f9-aa6b-29ae8df64a90">Tint::SetParameters</a> method of a <b>Tint</b> object.

