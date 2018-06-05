---
UID: NF:vfw.capSetCallbackOnError
title: capSetCallbackOnError macro
author: windows-sdk-content
description: The capSetCallbackOnError macro sets an error callback function in the client application. AVICap calls this procedure when errors occur. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_ERROR message.
old-location: multimedia\capsetcallbackonerror.htm
old-project: Multimedia
ms.assetid: 1f9d3dba-be6d-4f7d-a80c-5bca8632e13f
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: "_win32_capSetCallbackOnError, capSetCallbackOnError, capSetCallbackOnError macro [Windows Multimedia], multimedia.capsetcallbackonerror, vfw/capSetCallbackOnError"
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
-	capSetCallbackOnError
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capSetCallbackOnError macro


## -description



The <b>capSetCallbackOnError</b> macro sets an error callback function in the client application. AVICap calls this procedure when errors occur. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4eb57515-9b5a-466c-bbaa-fdee3bca19db">WM_CAP_SET_CALLBACK_ERROR</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the error callback function, of type <a href="https://msdn.microsoft.com/3dc41a0e-1fed-423d-b05b-c42f361a3fb3">capErrorCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed error callback function. 


## -remarks



Applications can optionally set an error callback function. If set, AVICap calls the error procedure in the following situations:

<ul>
<li>The disk is full.</li>
<li>A capture window cannot be connected with a capture driver.</li>
<li>A waveform-audio device cannot be opened.</li>
<li>The number of frames dropped during capture exceeds the specified percentage.</li>
<li>The frames cannot be captured due to vertical synchronization interrupt problems.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a489ec94-c566-44b1-aa93-9b43f23de744">Creating an Error Callback Function</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>



<a href="https://msdn.microsoft.com/4eb57515-9b5a-466c-bbaa-fdee3bca19db">WM_CAP_SET_CALLBACK_ERROR</a>



<a href="https://msdn.microsoft.com/3dc41a0e-1fed-423d-b05b-c42f361a3fb3">capErrorCallback</a>
 

 

