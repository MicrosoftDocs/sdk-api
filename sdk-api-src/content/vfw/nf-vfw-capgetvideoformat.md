---
UID: NF:vfw.capGetVideoFormat
title: capGetVideoFormat macro (vfw.h)
description: The capGetVideoFormat macro retrieves a copy of the video format in use. You can use this macro or explicitly call the WM_CAP_GET_VIDEOFORMAT message.helpviewer_keywords: ["_win32_capGetVideoFormat","capGetVideoFormat","capGetVideoFormat macro [Windows Multimedia]","multimedia.capgetvideoformat","vfw/capGetVideoFormat"]
old-location: multimedia\capgetvideoformat.htm
tech.root: Multimedia
ms.assetid: 2013bf9c-3759-440a-a62c-2ba3c54441c1
ms.date: 12/05/2018
ms.keywords: _win32_capGetVideoFormat, capGetVideoFormat, capGetVideoFormat macro [Windows Multimedia], multimedia.capgetvideoformat, vfw/capGetVideoFormat
f1_keywords:
- vfw/capGetVideoFormat
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
- capGetVideoFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capGetVideoFormat macro


## -description



The <b>capGetVideoFormat</b> macro retrieves a copy of the video format in use. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-get-videoformat">WM_CAP_GET_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. You can also specify <b>NULL</b> to retrieve the number of bytes needed by <b>BITMAPINFO</b>. 


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


## -remarks



Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

