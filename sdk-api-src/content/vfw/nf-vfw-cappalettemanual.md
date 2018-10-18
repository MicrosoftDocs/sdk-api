---
UID: NF:vfw.capPaletteManual
title: capPaletteManual macro
author: windows-sdk-content
description: The capPaletteManual macro requests that the capture driver manually sample video frames and create a new palette. You can use this macro or explicitly call the WM_CAP_PAL_MANUALCREATE message.
old-location: multimedia\cappalettemanual.htm
tech.root: Multimedia
ms.assetid: 81dc204a-36a5-45eb-8c29-a6004d3cd49c
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "_win32_capPaletteManual, capPaletteManual, capPaletteManual macro [Windows Multimedia], multimedia.cappalettemanual, vfw/capPaletteManual"
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
 - capPaletteManual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capPaletteManual macro


## -description



The <b>capPaletteManual</b> macro requests that the capture driver manually sample video frames and create a new palette. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/96b6b2d6-084a-411e-8495-ea27e0c4f04f">WM_CAP_PAL_MANUALCREATE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fGrab

Palette histogram flag. Set this parameter to <b>TRUE</b> for each frame included in creating the optimal palette. After the last frame has been collected, set this parameter to <b>FALSE</b> to calculate the optimal palette and send it to the capture driver. 


### -param iColors

Number of colors in the palette. The maximum value for this parameter is 256. This value is used only during collection of the first frame in a sequence. 


## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

