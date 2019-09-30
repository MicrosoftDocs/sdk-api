---
UID: NF:amvideo.COLORS
title: COLORS macro (amvideo.h)
author: windows-sdk-content
description: The COLORS macro retrieves the palette entries from a VIDEOINFO structure.
old-location: dshow\colors.htm
tech.root: DirectShow
ms.assetid: 32541ee4-53ef-4f0a-b823-bb475a93a195
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COLORS, COLORS function [DirectShow], amvideo/COLORS, dshow.colors
ms.topic: macro
f1_keywords: 
 - "amvideo/COLORS"
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
req.lib: Strmbase.lib (retail builds); Strmbasd.lib (debug builds)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Strmbase.lib
 - Strmbase.dll
 - Strmbasd.lib
 - Strmbasd.dll
api_name:
 - COLORS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# COLORS macro


## -description


The COLORS macro retrieves the palette entries from a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure. 


## -parameters




### -param pbmi

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure. 


## -remarks



This macro calculates the address as an offset from the start of the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, using the value of <b>bmiHeader.biSize</b>. Make sure to initialize the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo">VIDEOINFO</a> structure before calling this macro.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-and-image-functions">Video and Image Functions</a>
 

 

