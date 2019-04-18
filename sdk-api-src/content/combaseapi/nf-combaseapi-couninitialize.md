---
UID: NF:combaseapi.CoUninitialize
title: CoUninitialize function (combaseapi.h)
author: windows-sdk-content
description: Closes the COM library on the current thread, unloads all DLLs loaded by the thread, frees any other resources that the thread maintains, and forces all RPC connections on the thread to close.
old-location: com\couninitialize.htm
tech.root: com
ms.assetid: 9411cbed-fa3b-46f7-b677-6ada53324edc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoUninitialize, CoUninitialize function [COM], _com_CoUninitialize, com.couninitialize, combaseapi/CoUninitialize
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoUninitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CoUninitialize function


## -description


Closes the COM library on the current thread, unloads all DLLs loaded by the thread, frees any other resources that the thread maintains, and forces all RPC connections on the thread to close.




## -parameters






## -returns



This function does not return a value.




## -remarks



A thread must call <b>CoUninitialize</b> once for each successful call it has made to the <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> function, including any call that returns S_FALSE. Only the <b>CoUninitialize</b> call corresponding to the <b>CoInitialize</b> or <b>CoInitializeEx</b> call that initialized the library can close it.



Calls to <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> must be balanced by calls to <a href="https://msdn.microsoft.com/b2a8233f-7e1b-4c54-9363-7478c40c3830">OleUninitialize</a>. The <b>OleUninitialize</b> function calls <b>CoUninitialize</b> internally, so applications that call <b>OleUninitialize</b> do not also need to call <b>CoUninitialize</b>.



<b>CoUninitialize</b> should be called on application shutdown, as the last call made to the COM library after the application hides its main windows and falls through its main message loop. If there are open conversations remaining, <b>CoUninitialize</b> starts a modal message loop and dispatches any pending messages from the containers or server for this COM application. By dispatching the messages, <b>CoUninitialize</b> ensures that the application does not quit before receiving all of its pending messages. Non-COM messages are discarded.



Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a>, <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, or <b>CoUninitialize</b> from the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a>



<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/b2a8233f-7e1b-4c54-9363-7478c40c3830">OleUninitialize</a>
 

 

