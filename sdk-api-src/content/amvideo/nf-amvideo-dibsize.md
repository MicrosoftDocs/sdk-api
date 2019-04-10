---
UID: NF:amvideo.DIBSIZE
title: DIBSIZE macro (amvideo.h)
author: windows-sdk-content
description: The DIBSIZE macro calculates the number of bytes required by a device-independent bitmap (DIB).
old-location: dshow\dibsize.htm
tech.root: DirectShow
ms.assetid: a1feaa57-f403-46d0-b9a4-56e94ff2ceee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DIBSIZE, DIBSIZE macro [DirectShow], amvideo/DIBSIZE, dshow.dibsize
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
 - DIBSIZE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DIBSIZE macro


## -description


The <code>DIBSIZE</code> macro calculates the number of bytes required by a device-independent bitmap (DIB). 


## -parameters




### -param bi

Specifies a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure.


## -remarks



The size of a DIB is calculated as <code>stride * height</code>, where stride is width * bits per pixel/8, rounded up to the nearest <b>DWORD</b> alignment; and height is the absolute value of <i>biHeight</i>.




## -see-also




<a href="https://msdn.microsoft.com/02401edc-362b-4f6c-b10b-c46b30b3ebe7">Video and Image Functions</a>
 

 

