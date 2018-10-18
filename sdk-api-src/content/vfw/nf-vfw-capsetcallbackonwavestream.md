---
UID: NF:vfw.capSetCallbackOnWaveStream
title: capSetCallbackOnWaveStream macro
author: windows-sdk-content
description: The capSetCallbackOnWaveStream macro sets a callback function in the application.
old-location: multimedia\capsetcallbackonwavestream.htm
tech.root: Multimedia
ms.assetid: 282386af-506b-4be6-bb75-aa3c62f9778a
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "_win32_capSetCallbackOnWaveStream, capSetCallbackOnWaveStream, capSetCallbackOnWaveStream macro [Windows Multimedia], multimedia.capsetcallbackonwavestream, vfw/capSetCallbackOnWaveStream"
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
 - capSetCallbackOnWaveStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capSetCallbackOnWaveStream macro


## -description



The <b>capSetCallbackOnWaveStream</b> macro sets a callback function in the application. AVICap calls this procedure during streaming capture when a new audio buffer becomes available. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/f2554cbb-73de-4f76-b785-6c18c82c2992">WM_CAP_SET_CALLBACK_WAVESTREAM</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the wave stream callback function, of type <a href="https://msdn.microsoft.com/e7047d3d-9393-4611-a034-d36d6e92ee01">capWaveStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed wave stream callback function. 


## -remarks



The capture window calls the procedure before writing the audio buffer to disk. This allows applications to modify the audio buffer if desired.

If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session. It can be disabled after streaming capture ends.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

