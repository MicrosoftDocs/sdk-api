---
UID: NF:vfw.capPaletteAuto
title: capPaletteAuto macro (vfw.h)
description: The capPaletteAuto macro requests that the capture driver sample video frames and automatically create a new palette. You can use this macro or explicitly call the WM_CAP_PAL_AUTOCREATE message.
helpviewer_keywords: ["_win32_capPaletteAuto","capPaletteAuto","capPaletteAuto macro [Windows Multimedia]","multimedia.cappaletteauto","vfw/capPaletteAuto"]
old-location: multimedia\cappaletteauto.htm
tech.root: Multimedia
ms.assetid: d83e7dbc-d063-4e76-a7a1-37eaf73b5e8a
ms.date: 12/05/2018
ms.keywords: _win32_capPaletteAuto, capPaletteAuto, capPaletteAuto macro [Windows Multimedia], multimedia.cappaletteauto, vfw/capPaletteAuto
f1_keywords:
- vfw/capPaletteAuto
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
- capPaletteAuto
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capPaletteAuto macro


## -description



The <b>capPaletteAuto</b> macro requests that the capture driver sample video frames and automatically create a new palette. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-pal-autocreate">WM_CAP_PAL_AUTOCREATE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param iFrames

Number of frames to sample. 


### -param iColors

Number of colors in the palette. The maximum value for this parameter is 256. 


## -remarks



The sampled video sequence should include all the colors you want in the palette. To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

