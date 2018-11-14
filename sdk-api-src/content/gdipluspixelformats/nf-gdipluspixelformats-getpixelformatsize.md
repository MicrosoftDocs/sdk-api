---
UID: NF:gdipluspixelformats.GetPixelFormatSize
title: GetPixelFormatSize function
author: windows-sdk-content
description: The GetPixelFormatSize method returns the number of bits per pixel used by a specified pixel format.
old-location: gdiplus\_gdiplus_FUNC_GetPixelFormatSize_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getpixelformatsize.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPixelFormatSize, GetPixelFormatSize function [GDI+], _gdiplus_FUNC_GetPixelFormatSize_, gdiplus._gdiplus_FUNC_GetPixelFormatSize_, gdipluspixelformats/GetPixelFormatSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gdipluspixelformats.h
req.include-header: Gdiplus.h
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
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetPixelFormatSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetPixelFormatSize
: 
req.product: GDI+ 1.1
---

# GetPixelFormatSize function


## -description


The <b>GetPixelFormatSize</b> method returns the number of bits per pixel used by a specified pixel format.


## -parameters




### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="https://msdn.microsoft.com/en-us/library/ms534412(v=VS.85).aspx">PixelFormat</a> constant that specifies the pixel format to be tested.


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the number of bits per pixel used by the specified pixel format.



