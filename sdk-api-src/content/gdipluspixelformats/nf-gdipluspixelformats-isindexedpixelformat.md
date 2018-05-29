---
UID: NF:gdipluspixelformats.IsIndexedPixelFormat
title: IsIndexedPixelFormat function
author: windows-sdk-content
description: The IsIndexedPixelFormat method determines whether a specified pixel format is an indexed format.
old-location: gdiplus\_gdiplus_FUNC_IsIndexedPixelFormat_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\isindexedpixelformat.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IsIndexedPixelFormat, IsIndexedPixelFormat function [GDI+], _gdiplus_FUNC_IsIndexedPixelFormat_, gdiplus._gdiplus_FUNC_IsIndexedPixelFormat_, gdipluspixelformats/IsIndexedPixelFormat
ms.prod: windows
ms.technology: windows-sdk
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
-	IsIndexedPixelFormat
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IsIndexedPixelFormat function


## -description


The <b>IsIndexedPixelFormat</b> method determines whether a specified pixel format is an indexed format.


## -parameters




### -param pixfmt

Type: <b>PixelFormat</b>

A <a href="https://msdn.microsoft.com/362204c5-5dd7-461a-b90b-15826c025689">PixelFormat</a> constant that specifies the pixel format to be tested.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the pixel format is an indexed format, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.



