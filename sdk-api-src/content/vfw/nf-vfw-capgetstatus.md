---
UID: NF:vfw.capGetStatus
title: capGetStatus macro
author: windows-sdk-content
description: The capGetStatus macro retrieves the status of the capture window. You can use this macro or explicitly call the WM_CAP_GET_STATUS message.
old-location: multimedia\capgetstatus.htm
old-project: Multimedia
ms.assetid: 5c974707-b6ca-4177-a262-6838d308fb0a
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: "_win32_capGetStatus, capGetStatus, capGetStatus macro [Windows Multimedia], multimedia.capgetstatus, vfw/capGetStatus"
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	capGetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capGetStatus macro


## -description



The <b>capGetStatus</b> macro retrieves the status of the capture window. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/31349599-a52c-45ba-8f08-91008773f317">WM_CAP_GET_STATUS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://msdn.microsoft.com/65ad6e33-c601-4026-a5a4-2c68576d7ab7">CAPSTATUS</a> structure.


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


## -remarks



The <a href="https://msdn.microsoft.com/65ad6e33-c601-4026-a5a4-2c68576d7ab7">CAPSTATUS</a> structure contains the current state of the capture window. Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the <a href="https://msdn.microsoft.com/542913e8-c3f4-4ea5-afa0-035af6f3126e">capDlgVideoFormat</a> macro and whenever it needs to enable menu items or determine the actual state of the window.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

