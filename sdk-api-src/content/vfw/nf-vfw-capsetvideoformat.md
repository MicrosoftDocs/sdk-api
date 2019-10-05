---
UID: NF:vfw.capSetVideoFormat
title: capSetVideoFormat macro (vfw.h)
author: windows-sdk-content
description: The capSetVideoFormat macro sets the format of captured video data. You can use this macro or explicitly call the WM_CAP_SET_VIDEOFORMAT message.
old-location: multimedia\capsetvideoformat.htm
tech.root: Multimedia
ms.assetid: 3c4bee26-d578-463b-8d97-6cdc78957ce0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capSetVideoFormat, capSetVideoFormat, capSetVideoFormat macro [Windows Multimedia], multimedia.capsetvideoformat, vfw/capSetVideoFormat"
ms.topic: macro
f1_keywords: 
 - "vfw/capSetVideoFormat"
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
 - capSetVideoFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capSetVideoFormat macro


## -description



The <b>capSetVideoFormat</b> macro sets the format of captured video data. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-videoformat">WM_CAP_SET_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. 


### -param wSize

The size, in bytes, of the structure referenced by <i>psVideoFormat</i>. 


## -remarks



Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

