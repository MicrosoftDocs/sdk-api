---
UID: NF:vfw.capFileSetCaptureFile
title: capFileSetCaptureFile macro (vfw.h)
description: The capFileSetCaptureFile macro names the file used for video capture. You can use this macro or explicitly call the WM_CAP_FILE_SET_CAPTURE_FILE message.
helpviewer_keywords: ["_win32_capFileSetCaptureFile","capFileSetCaptureFile","capFileSetCaptureFile macro [Windows Multimedia]","multimedia.capfilesetcapturefile","vfw/capFileSetCaptureFile"]
old-location: multimedia\capfilesetcapturefile.htm
tech.root: Multimedia
ms.assetid: 47c69c62-5455-401e-adba-9a0eced548cf
ms.date: 12/05/2018
ms.keywords: _win32_capFileSetCaptureFile, capFileSetCaptureFile, capFileSetCaptureFile macro [Windows Multimedia], multimedia.capfilesetcapturefile, vfw/capFileSetCaptureFile
f1_keywords:
- vfw/capFileSetCaptureFile
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
- capFileSetCaptureFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capFileSetCaptureFile macro


## -description



The <b>capFileSetCaptureFile</b> macro names the file used for video capture. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-file-set-capture-file">WM_CAP_FILE_SET_CAPTURE_FILE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to the null-terminated string that contains the name of the capture file to use. 


## -remarks



This message stores the filename in an internal structure. It does not create, allocate, or open the specified file. The default capture filename is C:\CAPTURE.AVI.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

