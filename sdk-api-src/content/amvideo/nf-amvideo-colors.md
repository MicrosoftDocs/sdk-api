---
UID: NF:amvideo.COLORS
title: COLORS macro
author: windows-driver-content
description: The COLORS macro retrieves the palette entries from a VIDEOINFO structure.
old-location: dshow\colors.htm
old-project: DirectShow
ms.assetid: 32541ee4-53ef-4f0a-b823-bb475a93a195
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: COLORS, COLORS function [DirectShow], amvideo/COLORS, dshow.colors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: amvideo.h
req.include-header: Streams.h
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Strmbase.lib
-	Strmbase.dll
-	Strmbasd.lib
-	Strmbasd.dll
api_name:
-	COLORS
product: Windows
targetos: Windows
req.lib: Strmbase.lib (retail builds); Strmbasd.lib (debug builds)
req.dll: 
req.irql: 
---

# COLORS macro


## -description


The COLORS macro retrieves the palette entries from a <a href="https://msdn.microsoft.com/f08a449c-fed4-400b-a2fc-817bd59ba3fd">VIDEOINFO</a> structure. 


## -parameters




### -param pbmi

Pointer to a <a href="https://msdn.microsoft.com/f08a449c-fed4-400b-a2fc-817bd59ba3fd">VIDEOINFO</a> structure. 


## -remarks



This macro calculates the address as an offset from the start of the <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure, using the value of <b>bmiHeader.biSize</b>. Make sure to initialize the <a href="https://msdn.microsoft.com/f08a449c-fed4-400b-a2fc-817bd59ba3fd">VIDEOINFO</a> structure before calling this macro.




## -see-also




<a href="https://msdn.microsoft.com/02401edc-362b-4f6c-b10b-c46b30b3ebe7">Video and Image Functions</a>
 

 

