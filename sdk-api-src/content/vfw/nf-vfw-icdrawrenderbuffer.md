---
UID: NF:vfw.ICDrawRenderBuffer
title: ICDrawRenderBuffer macro
author: windows-sdk-content
description: The ICDrawRenderBuffer macro notifies a rendering driver to draw the frames that have been passed to it. You can use this macro or explicitly call the ICM_DRAW_RENDERBUFFER message.
old-location: multimedia\icdrawrenderbuffer.htm
tech.root: Multimedia
ms.assetid: dc87dd00-1a48-4434-894c-fb49d4e92d20
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ICDrawRenderBuffer, ICDrawRenderBuffer macro [Windows Multimedia], _win32_ICDrawRenderBuffer, multimedia.icdrawrenderbuffer, vfw/ICDrawRenderBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICDrawRenderBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawRenderBuffer macro


## -description



The <b>ICDrawRenderBuffer</b> macro notifies a rendering driver to draw the frames that have been passed to it. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9">ICM_DRAW_RENDERBUFFER</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.

This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

