---
UID: NF:vfw.ICDrawWindow
title: ICDrawWindow macro
author: windows-sdk-content
description: The ICDrawWindow macro notifies a rendering driver that the window specified for the ICM_DRAW_BEGIN message needs to be redrawn. The window has moved or become temporarily obscured. You can use this macro or explicitly call the ICM_DRAW_WINDOW message.
old-location: multimedia\icdrawwindow.htm
old-project: Multimedia
ms.assetid: 35f799f6-99ce-41a4-9165-3bb614ea01d5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICDrawWindow, ICDrawWindow macro [Windows Multimedia], _win32_ICDrawWindow, multimedia.icdrawwindow, vfw/ICDrawWindow
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
 - ICDrawWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDrawWindow macro


## -description



The <b>ICDrawWindow</b> macro notifies a rendering driver that the window specified for the <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> message needs to be redrawn. The window has moved or become temporarily obscured. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4df1b9a7-8d61-4e79-8f43-1e7ee266375c">ICM_DRAW_WINDOW</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param prc

Pointer to the destination rectangle in screen coordinates. If this parameter points to an empty rectangle, drawing should be turned off. 


## -remarks



This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.

Video-overlay drivers use this message to draw when the window is obscured or moved. When a window specified for <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> is completely hidden by other windows, the destination rectangle is empty. Drivers should turn off video-overlay hardware when this condition occurs.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

