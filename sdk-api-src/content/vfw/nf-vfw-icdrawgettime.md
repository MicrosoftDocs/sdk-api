---
UID: NF:vfw.ICDrawGetTime
title: ICDrawGetTime macro (vfw.h)
description: The ICDrawGetTime macro requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock. You can use this macro or explicitly call the ICM_DRAW_GETTIME message.helpviewer_keywords: ["ICDrawGetTime","ICDrawGetTime macro [Windows Multimedia]","_win32_ICDrawGetTime","multimedia.icdrawgettime","vfw/ICDrawGetTime"]
old-location: multimedia\icdrawgettime.htm
tech.root: Multimedia
ms.assetid: ebf21b97-7bfe-4eca-9442-9fc4db663ac6
ms.date: 12/05/2018
ms.keywords: ICDrawGetTime, ICDrawGetTime macro [Windows Multimedia], _win32_ICDrawGetTime, multimedia.icdrawgettime, vfw/ICDrawGetTime
f1_keywords:
- vfw/ICDrawGetTime
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vfw.h
api_name:
- ICDrawGetTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDrawGetTime macro


## -description



The <b>ICDrawGetTime</b> macro requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-draw-gettime">ICM_DRAW_GETTIME</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lplTime

Address to contain the current time. The return value should be specified in samples. 


## -remarks



This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing. The message can also be sent if the hardware is being used as the synchronization master.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

