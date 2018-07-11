---
UID: NL:gdipluseffects.Levels
title: Levels
author: windows-sdk-content
description: The Levels class encompasses three bitmap adjustments:\_highlight, midtone, and shadow.
old-location: gdiplus\_gdiplus_CLASS_Levels_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\levels.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Levels, Levels class [GDI+], Levels class [GDI+],described, _gdiplus_CLASS_Levels_Class, gdiplus._gdiplus_CLASS_Levels_Class, gdipluseffects/Levels
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
 - Levels
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Levels class


## -description


The <b>Levels</b> class encompasses three bitmap adjustments: highlight, midtone, and shadow. You can apply one or more of those adjustments to a bitmap by passing the address of a <b>Levels</b> object to the <a href="https://msdn.microsoft.com/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the intensities of the adjustments, pass the address of a <a href="https://msdn.microsoft.com/library/ms534070(v=VS.85).aspx">LevelsParams</a> structure to the <a href="https://msdn.microsoft.com/library/ms535361(v=VS.85).aspx">Levels::SetParameters</a> method of a <b>Levels</b> object.

