---
UID: NF:vfw.capCaptureSetSetup
title: capCaptureSetSetup macro (vfw.h)
description: The capCaptureSetSetup macro sets the configuration parameters used with streaming capture. You can use this macro or explicitly send the WM_CAP_SET_SEQUENCE_SETUP message.
helpviewer_keywords: ["_win32_capCaptureSetSetup","capCaptureSetSetup","capCaptureSetSetup macro [Windows Multimedia]","multimedia.capcapturesetsetup","vfw/capCaptureSetSetup"]
old-location: multimedia\capcapturesetsetup.htm
tech.root: Multimedia
ms.assetid: 663dcb34-6b11-4208-b5d6-216799fb774d
ms.date: 12/05/2018
ms.keywords: _win32_capCaptureSetSetup, capCaptureSetSetup, capCaptureSetSetup macro [Windows Multimedia], multimedia.capcapturesetsetup, vfw/capCaptureSetSetup
f1_keywords:
- vfw/capCaptureSetSetup
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
- capCaptureSetSetup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capCaptureSetSetup macro


## -description



The <b>capCaptureSetSetup</b> macro sets the configuration parameters used with streaming capture. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-sequence-setup">WM_CAP_SET_SEQUENCE_SETUP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a CAPTUREPARMS structure. 


### -param wSize

Size, in bytes, of the structure referenced by s. 


## -remarks



For information about the parameters used to control streaming capture, see the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-captureparms">CAPTUREPARMS</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

