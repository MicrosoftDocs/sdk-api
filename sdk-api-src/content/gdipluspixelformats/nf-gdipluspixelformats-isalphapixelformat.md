---
UID: NF:gdipluspixelformats.IsAlphaPixelFormat
title: IsAlphaPixelFormat function
author: windows-sdk-content
description: The IsAlphaPixelFormat method determines whether a specified pixel format has an alpha component.
old-location: gdiplus\_gdiplus_FUNC_IsAlphaPixelFormat_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\isalphapixelformat.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IsAlphaPixelFormat, IsAlphaPixelFormat function [GDI+], _gdiplus_FUNC_IsAlphaPixelFormat_, gdiplus._gdiplus_FUNC_IsAlphaPixelFormat_, gdipluspixelformats/IsAlphaPixelFormat
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
 - IsAlphaPixelFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsAlphaPixelFormat
: 
req.product: GDI+ 1.1
---

# IsAlphaPixelFormat function


## -description


The <b>IsAlphaPixelFormat</b> method determines whether a specified pixel format has an alpha component.


## -parameters




### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">PixelFormat</a> constant that specifies the pixel format to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the pixel format has an alpha component, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.



