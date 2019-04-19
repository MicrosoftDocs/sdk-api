---
UID: NF:vfw.ICDrawFlush
title: ICDrawFlush macro (vfw.h)
author: windows-sdk-content
description: The ICDrawFlush macro notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn. You can use this macro or explicitly call the ICM_DRAW_FLUSH message.
old-location: multimedia\icdrawflush.htm
tech.root: Multimedia
ms.assetid: ceff1075-4e23-4be0-aac0-27fc5fe68083
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICDrawFlush, ICDrawFlush macro [Windows Multimedia], _win32_ICDrawFlush, multimedia.icdrawflush, vfw/ICDrawFlush
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
 - ICDrawFlush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDrawFlush macro


## -description



The <b>ICDrawFlush</b> macro notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/c29ed751-c773-4476-98fe-6edef3ff0cf4">ICM_DRAW_FLUSH</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

