---
UID: NF:vfw.capPaletteAuto
title: capPaletteAuto macro
author: windows-sdk-content
description: The capPaletteAuto macro requests that the capture driver sample video frames and automatically create a new palette. You can use this macro or explicitly call the WM_CAP_PAL_AUTOCREATE message.
old-location: multimedia\cappaletteauto.htm
old-project: Multimedia
ms.assetid: d83e7dbc-d063-4e76-a7a1-37eaf73b5e8a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_win32_capPaletteAuto, capPaletteAuto, capPaletteAuto macro [Windows Multimedia], multimedia.cappaletteauto, vfw/capPaletteAuto"
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
 - capPaletteAuto
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capPaletteAuto macro


## -description



The <b>capPaletteAuto</b> macro requests that the capture driver sample video frames and automatically create a new palette. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/b94d245d-adf4-4fe0-b053-87109ef5fd2f">WM_CAP_PAL_AUTOCREATE</a> message.




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




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

