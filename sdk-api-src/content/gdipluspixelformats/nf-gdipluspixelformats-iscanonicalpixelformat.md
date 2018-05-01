---
UID: NF:gdipluspixelformats.IsCanonicalPixelFormat
title: IsCanonicalPixelFormat function
author: windows-driver-content
description: The IsCanonicalPixelFormat method determines whether a specified pixel format is one of the canonical formats:\_PixelFormat32bppARGB or PixelFormat64bppARGB.
old-location: gdiplus\_gdiplus_FUNC_IsCanonicalPixelFormat_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\iscanonicalpixelformat.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IsCanonicalPixelFormat, IsCanonicalPixelFormat function [GDI+], _gdiplus_FUNC_IsCanonicalPixelFormat_, gdiplus._gdiplus_FUNC_IsCanonicalPixelFormat_, gdipluspixelformats/IsCanonicalPixelFormat
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	IsCanonicalPixelFormat
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IsCanonicalPixelFormat function


## -description


The <b>IsCanonicalPixelFormat</b> method determines whether a specified pixel format is one of the canonical formats: <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">PixelFormat32bppARGB</a> or <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">PixelFormat64bppARGB</a>.


## -parameters




### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">PixelFormat</a> constant that specifies the pixel format to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the pixel format is <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">PixelFormat32bppARGB</a> or <b>PixelFormat64bppARGB</b>, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.



