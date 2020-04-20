---
UID: NF:vfw.capSetScrollPos
title: capSetScrollPos macro (vfw.h)
description: The capSetScrollPos macro defines the portion of the video frame to display in the capture window.helpviewer_keywords: ["_win32_capSetScrollPos","capSetScrollPos","capSetScrollPos macro [Windows Multimedia]","multimedia.capsetscrollpos","vfw/capSetScrollPos"]
old-location: multimedia\capsetscrollpos.htm
tech.root: Multimedia
ms.assetid: a5af0d75-ae9f-41f2-90cb-8ede7c2f454a
ms.date: 12/05/2018
ms.keywords: _win32_capSetScrollPos, capSetScrollPos, capSetScrollPos macro [Windows Multimedia], multimedia.capsetscrollpos, vfw/capSetScrollPos
f1_keywords:
- vfw/capSetScrollPos
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
- capSetScrollPos
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capSetScrollPos macro


## -description



The <b>capSetScrollPos</b> macro defines the portion of the video frame to display in the capture window. This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-scroll">WM_CAP_SET_SCROLL</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param lpP

Address to contain the desired scroll position. 


## -remarks



The scroll position affects the image in both preview and overlay modes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

