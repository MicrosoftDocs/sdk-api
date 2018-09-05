---
UID: NF:dwrite_1.IDWriteFontFace1.GetCaretMetrics
title: IDWriteFontFace1::GetCaretMetrics
author: windows-sdk-content
description: Gets caret metrics for the font in design units.
old-location: directwrite\idwritefontface1_getcaretmetrics.htm
old-project: DirectWrite
ms.assetid: D9006617-A5B5-4575-9C00-26F52A73DC0D
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetCaretMetrics, GetCaretMetrics method [Direct Write], GetCaretMetrics method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetCaretMetrics method, IDWriteFontFace1.GetCaretMetrics, IDWriteFontFace1::GetCaretMetrics, directwrite.idwritefontface1_getcaretmetrics, dwrite_1/IDWriteFontFace1::GetCaretMetrics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.GetCaretMetrics
product: Windows
targetos: Windows
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFace1::GetCaretMetrics


## -description


Gets caret metrics for the font in design units.


## -parameters




### -param caretMetrics [out]

Type: <b>DWRITE_CARET_METRICS*</b>

A pointer to the <a href="https://msdn.microsoft.com/CC7591F8-0671-436F-B0A7-C5D4C183D253">DWRITE_CARET_METRICS</a> structure that is filled.


## -returns



This method does not return a value.




## -remarks



Caret metrics are used by
    text editors for drawing the correct caret placement and slant.




## -see-also




<a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>
 

 

