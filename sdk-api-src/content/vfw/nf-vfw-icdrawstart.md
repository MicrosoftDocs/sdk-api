---
UID: NF:vfw.ICDrawStart
title: ICDrawStart macro
author: windows-sdk-content
description: The ICDrawStart macro notifies a rendering driver to start its internal clock for the timing of drawing frames. You can use this macro or explicitly call the ICM_DRAW_START message.
old-location: multimedia\icdrawstart.htm
tech.root: Multimedia
ms.assetid: 00db96a3-d7e4-42eb-929a-c967ac8380d1
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ICDrawStart, ICDrawStart macro [Windows Multimedia], _win32_ICDrawStart, multimedia.icdrawstart, vfw/ICDrawStart
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
 - ICDrawStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawStart macro


## -description



The <b>ICDrawStart</b> macro notifies a rendering driver to start its internal clock for the timing of drawing frames. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/d49e0d97-5a29-46f7-82d7-e3d4b4f7666f">ICM_DRAW_START</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.

When the driver receives this message, it should start rendering data at the rate specified with the <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> message.

The <b>ICDrawStart</b> and <a href="https://msdn.microsoft.com/c8608410-da45-4953-b16a-050870f85af9">ICDrawStop</a> macros do not nest. If your driver receives <b>ICDrawStart</b> before rendering is stopped with <b>ICDrawStop</b>, it should restart rendering with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

