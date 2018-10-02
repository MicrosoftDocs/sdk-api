---
UID: NF:vfw.capPreview
title: capPreview macro
author: windows-sdk-content
description: The capPreview macro enables or disables preview mode.
old-location: multimedia\cappreview.htm
tech.root: Multimedia
ms.assetid: c6888e35-9915-4ffb-ac0d-3cc1419fdac3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "_win32_capPreview, capPreview, capPreview macro [Windows Multimedia], multimedia.cappreview, vfw/capPreview"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - capPreview
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capPreview macro


## -description



The <b>capPreview</b> macro enables or disables preview mode. In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/ef6218d6-4fff-469f-b2e0-d7990998a3e5">WM_CAP_SET_PREVIEW</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param f

Preview flag. Specify <b>TRUE</b> for this parameter to enable preview mode or <b>FALSE</b> to disable it. 


## -remarks



The preview mode uses substantial CPU resources. Applications can disable preview or lower the preview rate when another application has the focus. The <b>fLiveWindow</b> member of the <a href="https://msdn.microsoft.com/65ad6e33-c601-4026-a5a4-2c68576d7ab7">CAPSTATUS</a> structure indicates if preview mode is currently enabled.

Enabling preview mode automatically disables overlay mode.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

