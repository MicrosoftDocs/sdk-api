---
UID: NF:vfw.capSetCallbackOnStatus
title: capSetCallbackOnStatus macro
author: windows-sdk-content
description: The capSetCallbackOnStatus macro sets a status callback function in the application. AVICap calls this procedure whenever the capture window status changes. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_STATUS message.
old-location: multimedia\capsetcallbackonstatus.htm
tech.root: Multimedia
ms.assetid: 7024aa3e-d227-4c22-8259-6299e9205f53
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "_win32_capSetCallbackOnStatus, capSetCallbackOnStatus, capSetCallbackOnStatus macro [Windows Multimedia], multimedia.capsetcallbackonstatus, vfw/capSetCallbackOnStatus"
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
 - capSetCallbackOnStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capSetCallbackOnStatus macro


## -description



The <b>capSetCallbackOnStatus</b> macro sets a status callback function in the application. AVICap calls this procedure whenever the capture window status changes. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/451ba9f9-7bfb-4c57-af6c-d5f691f39618">WM_CAP_SET_CALLBACK_STATUS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the status callback function, of type <a href="https://msdn.microsoft.com/b48021a7-7fa1-4837-a6ca-af266fd55f4f">capStatusCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed status callback function. 


## -remarks



Applications can optionally set a status callback function. If set, AVICap calls this procedure in the following situations:

<ul>
<li>A capture session is completed.</li>
<li>A capture driver successfully connected to a capture window.</li>
<li>An optimal palette is created.</li>
<li>The number of captured frames is reported.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9aa98340-a5a0-4084-9670-b3c27a1351ed">Creating a Status Callback Function</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

