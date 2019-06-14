---
UID: NF:vfw.capPaletteOpen
title: capPaletteOpen macro (vfw.h)
author: windows-sdk-content
description: The capPaletteOpen macro loads a new palette from a palette file and passes it to a capture driver.
old-location: multimedia\cappaletteopen.htm
tech.root: Multimedia
ms.assetid: 1d50795e-c414-4bf5-a255-76532a34d944
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capPaletteOpen, capPaletteOpen, capPaletteOpen macro [Windows Multimedia], multimedia.cappaletteopen, vfw/capPaletteOpen"
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
 - capPaletteOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capPaletteOpen macro


## -description



The <b>capPaletteOpen</b> macro loads a new palette from a palette file and passes it to a capture driver. Palette files typically use the filename extension .PAL. A capture driver uses a palette when required by the specified digitized image format. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-pal-open">WM_CAP_PAL_OPEN</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string containing the palette filename. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

