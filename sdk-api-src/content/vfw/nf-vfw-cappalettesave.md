---
UID: NF:vfw.capPaletteSave
title: capPaletteSave macro (vfw.h)
description: The capPaletteSave macro saves the current palette to a palette file. Palette files typically use the filename extension .PAL. You can use this macro or explicitly send the WM_CAP_PAL_SAVE message.
helpviewer_keywords: ["_win32_capPaletteSave","capPaletteSave","capPaletteSave macro [Windows Multimedia]","multimedia.cappalettesave","vfw/capPaletteSave"]
old-location: multimedia\cappalettesave.htm
tech.root: Multimedia
ms.assetid: 11309b32-bc42-41fd-a0cd-e356caade849
ms.date: 12/05/2018
ms.keywords: _win32_capPaletteSave, capPaletteSave, capPaletteSave macro [Windows Multimedia], multimedia.cappalettesave, vfw/capPaletteSave
f1_keywords:
- vfw/capPaletteSave
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
- capPaletteSave
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capPaletteSave macro


## -description



The <b>capPaletteSave</b> macro saves the current palette to a palette file. Palette files typically use the filename extension .PAL. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-pal-save">WM_CAP_PAL_SAVE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string containing the palette filename. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

