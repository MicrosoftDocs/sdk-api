---
UID: NF:vfw.ICDrawSetTime
title: ICDrawSetTime macro
author: windows-sdk-content
description: The ICDrawSetTime macro provides synchronization information to a rendering driver that handles the timing of drawing frames.
old-location: multimedia\icdrawsettime.htm
old-project: Multimedia
ms.assetid: 4c97e0ee-c6f1-4258-9a5f-de633f8c0335
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICDrawSetTime, ICDrawSetTime macro [Windows Multimedia], _win32_ICDrawSetTime, multimedia.icdrawsettime, vfw/ICDrawSetTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: vfw.h
req.include-header: 
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDrawSetTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDrawSetTime macro


## -description



The <b>ICDrawSetTime</b> macro provides synchronization information to a rendering driver that handles the timing of drawing frames. The synchronization information is the sample number of the frame to draw. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/211e8ecc-ef36-4598-aa1d-cb0a06e64f14">ICM_DRAW_SETTIME</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lTime

Sample number of the frame to render. 


## -remarks



Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.

Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

