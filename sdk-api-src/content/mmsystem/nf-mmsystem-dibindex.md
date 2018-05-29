---
UID: NF:mmsystem.DIBINDEX
title: DIBINDEX macro
author: windows-sdk-content
description: The DIBINDEX macro takes an index to an entry in a DIB color table and returns a COLORREF value that specifies the color associated with the given index.
old-location: gdi\dibindex.htm
old-project: gdi
ms.assetid: a1c2274e-ddcb-4e11-af70-9f79210d2d5f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DIBINDEX, DIBINDEX macro [Windows GDI], _win32_DIBINDEX, gdi.dibindex, mmsystem/DIBINDEX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: mmsystem.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAM_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mmsystem.h
api_name:
-	DIBINDEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DIBINDEX macro


## -description



The <b>DIBINDEX</b> macro takes an index to an entry in a DIB color table and returns a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that specifies the color associated with the given index. An application using a device context with a DIB section selected into it can pass this specifier, instead of an explicit red, green, blue (RGB) value, to GDI functions that expect a color. This allows the function to use the color at the specified color table index.




## -parameters




### -param n

TBD






#### - wColorTableIndex

Specifies an index to the color table entry containing the color to be used for a graphics operation.


## -remarks



<b>DIBINDEX</b> indexes colors in a DIB color table in a manner similar to the way <a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a> indexes colors in a logical palette.

<b>DIBINDEX</b> also works with 16-bit bitmaps and device contexts (DCs).




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/f5bded0f-5f55-4512-9c00-9a9eb08c39f0">Color Macros</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

