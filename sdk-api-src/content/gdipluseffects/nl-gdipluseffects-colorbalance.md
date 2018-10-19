---
UID: NL:gdipluseffects.ColorBalance
title: ColorBalance
author: windows-sdk-content
description: The ColorBalance class enables you to change the color balance (relative amounts of red, green, and blue) of a bitmap.
old-location: gdiplus\_gdiplus_CLASS_ColorBalance_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorbalance.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ColorBalance, ColorBalance class [GDI+], ColorBalance class [GDI+],described, _gdiplus_CLASS_ColorBalance_Class, gdiplus._gdiplus_CLASS_ColorBalance_Class, gdipluseffects/ColorBalance
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
 - ColorBalance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ColorBalance class


## -description


The <b>ColorBalance</b> class enables you to change the color balance (relative amounts of red, green, and blue) of a bitmap. Pass the address of a <b>ColorBalance</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. To specify the nature of the change, pass the address of a <a href="https://msdn.microsoft.com/en-us/library/ms534059(v=VS.85).aspx">ColorBalanceParams</a> structure to the <a href="https://msdn.microsoft.com/en-us/library/ms536264(v=VS.85).aspx">ColorBalance::SetParameters</a> method of a <b>ColorBalance</b> object.

