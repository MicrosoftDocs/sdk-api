---
UID: NL:gdipluseffects.ColorLUT
title: ColorLUT
author: windows-sdk-content
description: A ColorLUTParams structure has four members, each being a lookup table for a particular color channel:\_alpha, red, green, or blue.
old-location: gdiplus\_gdiplus_CLASS_ColorLUT_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorlut.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ColorLUT, ColorLUT class [GDI+], ColorLUT class [GDI+],described, _gdiplus_CLASS_ColorLUT_Class, gdiplus._gdiplus_CLASS_ColorLUT_Class, gdipluseffects/ColorLUT
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
 - ColorLUT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ColorLUT class


## -description


A <a href="https://msdn.microsoft.com/en-us/library/ms534061(v=VS.85).aspx">ColorLUTParams</a> structure has four members, each being a lookup table for a particular color channel: alpha, red, green, or blue. The lookup tables can be used to make custom color adjustments to bitmaps. Each lookup table is an array of 256 bytes that you can set to values of your choice. After you have initialized a <b>ColorLUTParams</b> structure, pass its address to the <a href="https://msdn.microsoft.com/en-us/library/ms536237(v=VS.85).aspx">ColorLUT::SetParameters</a> method of a <b>ColorLUT</b> object. Then pass the address of that <b>ColorLUT</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.

