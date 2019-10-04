---
UID: NF:vfw.capCaptureGetSetup
title: capCaptureGetSetup macro (vfw.h)
author: windows-sdk-content
description: The capCaptureGetSetup macro retrieves the current settings of the streaming capture parameters. You can use this macro or explictly send the WM_CAP_GET_SEQUENCE_SETUP message.
old-location: multimedia\capcapturegetsetup.htm
tech.root: Multimedia
ms.assetid: 198b1aae-b719-4fb8-a11d-859eaf7a4606
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capCaptureGetSetup, capCaptureGetSetup, capCaptureGetSetup macro [Windows Multimedia], multimedia.capcapturegetsetup, vfw/capCaptureGetSetup"
ms.topic: macro
f1_keywords: 
 - "vfw/capCaptureGetSetup"
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
 - capCaptureGetSetup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capCaptureGetSetup macro


## -description



The <b>capCaptureGetSetup</b> macro retrieves the current settings of the streaming capture parameters. You can use this macro or explictly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-get-sequence-setup">WM_CAP_GET_SEQUENCE_SETUP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure. 


### -param wSize

Size, in bytes, of the structure referenced by s. 


## -remarks



For information about the parameters used to control streaming capture, see the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

