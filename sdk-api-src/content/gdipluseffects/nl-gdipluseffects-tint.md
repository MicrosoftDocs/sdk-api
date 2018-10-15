---
UID: NL:gdipluseffects.Tint
title: Tint
author: windows-sdk-content
description: The Tint class enables you to apply a tint to a bitmap.
old-location: gdiplus\_gdiplus_CLASS_Tint_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\tint.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
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
 - Tint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Tint class


## -description


The <b>Tint</b> class enables you to apply a tint to a bitmap. Pass the address of a <b>Tint</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the nature of the tint, pass the address of a <a href="https://msdn.microsoft.com/en-us/library/ms534074(v=VS.85).aspx">TintParams</a> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms534518(v=VS.85).aspx">Tint::SetParameters</a> method of a <b>Tint</b> object.

