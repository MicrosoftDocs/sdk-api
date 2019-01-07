---
UID: NE:uxtheme._BP_BUFFERFORMAT
title: BP_BUFFERFORMAT
author: windows-sdk-content
description: Specifies the format of the buffer. Used by BeginBufferedAnimation and BeginBufferedPaint.
old-location: controls\BP_BUFFERFORMAT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\enums\bp_bufferformat.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BPBF_COMPATIBLEBITMAP, BPBF_DIB, BPBF_TOPDOWNDIB, BPBF_TOPDOWNMONODIB, BP_BUFFERFORMAT, BP_BUFFERFORMAT enumeration [Windows Controls], _shell_BP_BUFFERFORMAT, _shell_BP_BUFFERFORMAT_cpp, controls.BP_BUFFERFORMAT, controls._shell_BP_BUFFERFORMAT, uxtheme/BPBF_COMPATIBLEBITMAP, uxtheme/BPBF_DIB, uxtheme/BPBF_TOPDOWNDIB, uxtheme/BPBF_TOPDOWNMONODIB, uxtheme/BP_BUFFERFORMAT
ms.topic: enum
req.header: uxtheme.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - BP_BUFFERFORMAT
product: Windows
targetos: Windows
req.typenames: BP_BUFFERFORMAT
req.redist: 
---

# BP_BUFFERFORMAT enumeration


## -description


Specifies the format of the buffer. Used by <a href="https://msdn.microsoft.com/ca7204b3-3166-4911-96f9-16a0f59ecb09">BeginBufferedAnimation</a> and <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>.


## -enum-fields




### -field BPBF_COMPATIBLEBITMAP

Compatible bitmap. The  number of bits per pixel is based on the color format of the device associated with the HDC specified with <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a> or <a href="https://msdn.microsoft.com/ca7204b3-3166-4911-96f9-16a0f59ecb09">BeginBufferedAnimation</a>—typically, this is the display device.


### -field BPBF_DIB

Bottom-up device-independent bitmap. The origin of the bitmap is the lower-left corner. Uses 32 bits per pixel.


### -field BPBF_TOPDOWNDIB

Top-down device-independent bitmap. The origin of the bitmap is the upper-left corner. Uses 32 bits per pixel.


### -field BPBF_TOPDOWNMONODIB

Top-down, monochrome, device-independent bitmap. Uses 1 bit per pixel.


## -see-also




<a href="https://msdn.microsoft.com/d2866beb-ff7a-4390-8651-e7bf458ddf88">CreateCompatibleBitmap</a>



<a href="https://msdn.microsoft.com/56b39a3d-48a4-4620-9652-ec41ea4d6423">Device-Independent Bitmaps</a>



<b>Other Resources</b>
 

 

