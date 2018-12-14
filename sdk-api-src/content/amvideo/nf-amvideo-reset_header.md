---
UID: NF:amvideo.RESET_HEADER
title: RESET_HEADER macro
author: windows-sdk-content
description: The RESET_HEADER macro fills a VIDEOINFOHEADER with zeroes. You can also use this macro to clear just the VIDEOINFOHEADER portion of a VIDEOINFO structure.
old-location: dshow\reset_header.htm
tech.root: DirectShow
ms.assetid: bd976ff0-fbfb-4911-bee6-d53044eb3d23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RESET_HEADER, RESET_HEADER macro [DirectShow], amvideo/RESET_HEADER, dshow.reset_header
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Amvideo.h
api_name:
 - RESET_HEADER
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RESET_HEADER macro


## -description



The <code>RESET_HEADER</code> macro fills a <a href="https://msdn.microsoft.com/en-us/library/Dd407325(v=VS.85).aspx">VIDEOINFOHEADER</a> with zeroes. You can also use this macro to clear just the <b>VIDEOINFOHEADER</b> portion of a <a href="https://msdn.microsoft.com/en-us/library/Dd407323(v=VS.85).aspx">VIDEOINFO</a> structure.



This macro is equivalent to calling <b>ZeroMemory</b> with <code>sizeof(VIDEOINFOHEADER)</code>.


## -parameters




### -param pbmi

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd407325(v=VS.85).aspx">VIDEOINFOHEADER</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/02401edc-362b-4f6c-b10b-c46b30b3ebe7">Video and Image Functions</a>
 

 

