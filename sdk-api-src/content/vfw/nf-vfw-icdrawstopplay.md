---
UID: NF:vfw.ICDrawStopPlay
title: ICDrawStopPlay macro
author: windows-sdk-content
description: The ICDrawStopPlay macro notifies a rendering driver when a play operation is complete. You can use this macro or explicitly call the ICM_DRAW_STOP_PLAY message.
old-location: multimedia\icdrawstopplay.htm
tech.root: Multimedia
ms.assetid: 41faa7cd-13c9-47bc-a62e-c09c7d3264d7
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ICDrawStopPlay, ICDrawStopPlay macro [Windows Multimedia], _win32_ICDrawStopPlay, multimedia.icdrawstopplay, vfw/ICDrawStopPlay
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
 - ICDrawStopPlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- vfw.h
: 
- ICDrawStopPlay
: 
---

# ICDrawStopPlay macro


## -description



The <b>ICDrawStopPlay</b> macro notifies a rendering driver when a play operation is complete. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/cfe2ee98-80d0-4554-bcbd-9873769da674">ICM_DRAW_STOP_PLAY</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



Use this message when the play operation is complete. Use the <a href="https://msdn.microsoft.com/c8608410-da45-4953-b16a-050870f85af9">ICDrawStop</a> macro to end timing.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

