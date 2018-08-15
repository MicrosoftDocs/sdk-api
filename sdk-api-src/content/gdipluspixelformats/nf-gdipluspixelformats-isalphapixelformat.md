---
UID: NF:gdipluspixelformats.IsAlphaPixelFormat
title: IsAlphaPixelFormat function
author: windows-sdk-content
description: The IsAlphaPixelFormat method determines whether a specified pixel format has an alpha component.
old-location: gdiplus\_gdiplus_FUNC_IsAlphaPixelFormat_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\isalphapixelformat.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IsAlphaPixelFormat, IsAlphaPixelFormat function [GDI+], _gdiplus_FUNC_IsAlphaPixelFormat_, gdiplus._gdiplus_FUNC_IsAlphaPixelFormat_, gdipluspixelformats/IsAlphaPixelFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: gdipluspixelformats.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - IsAlphaPixelFormat
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IsAlphaPixelFormat function


## -description


The <b>IsAlphaPixelFormat</b> method determines whether a specified pixel format has an alpha component.


## -parameters




### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">PixelFormat</a> constant that specifies the pixel format to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the pixel format has an alpha component, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.



