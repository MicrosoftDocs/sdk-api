---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

