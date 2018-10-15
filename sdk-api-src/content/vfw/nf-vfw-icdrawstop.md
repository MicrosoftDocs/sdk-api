---
UID: NF:vfw.ICDrawStop
title: ICDrawStop macro
author: windows-sdk-content
description: The ICDrawStop macro notifies a rendering driver to stop its internal clock for the timing of drawing frames. You can use this macro or explicitly call the ICM_DRAW_STOP message.
old-location: multimedia\icdrawstop.htm
tech.root: Multimedia
ms.assetid: c8608410-da45-4953-b16a-050870f85af9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ICDrawStop, ICDrawStop macro [Windows Multimedia], _win32_ICDrawStop, multimedia.icdrawstop, vfw/ICDrawStop
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
 - ICDrawStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawStop macro


## -description



The <b>ICDrawStop</b> macro notifies a rendering driver to stop its internal clock for the timing of drawing frames. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/9ffda595-e3d6-48f0-9487-69f7e95979c2">ICM_DRAW_STOP</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



This macro is used by hardware that performs its own asynchronous decompression, timing, and drawing.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

