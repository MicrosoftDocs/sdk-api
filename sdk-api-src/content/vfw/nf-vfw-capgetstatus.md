---
UID: NF:vfw.capGetStatus
title: capGetStatus macro (vfw.h)
author: windows-sdk-content
description: The capGetStatus macro retrieves the status of the capture window. You can use this macro or explicitly call the WM_CAP_GET_STATUS message.
old-location: multimedia\capgetstatus.htm
tech.root: Multimedia
ms.assetid: 5c974707-b6ca-4177-a262-6838d308fb0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capGetStatus, capGetStatus, capGetStatus macro [Windows Multimedia], multimedia.capgetstatus, vfw/capGetStatus"
ms.topic: macro
f1_keywords: 
 - "vfw/capGetStatus"
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
 - capGetStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capGetStatus macro


## -description



The <b>capGetStatus</b> macro retrieves the status of the capture window. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-get-status">WM_CAP_GET_STATUS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-capstatus">CAPSTATUS</a> structure.


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-capstatus">CAPSTATUS</a> structure contains the current state of the capture window. Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capdlgvideoformat">capDlgVideoFormat</a> macro and whenever it needs to enable menu items or determine the actual state of the window.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

