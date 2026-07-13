---
UID: NF:combaseapi.CoUninitialize
title: CoUninitialize function (combaseapi.h)
description: Closes the COM library on the current thread, unloads all DLLs loaded by the thread, frees any other resources that the thread maintains, and forces all RPC connections on the thread to close.
helpviewer_keywords: ["CoUninitialize","CoUninitialize function [COM]","_com_CoUninitialize","com.couninitialize","combaseapi/CoUninitialize"]
old-location: com\couninitialize.htm
tech.root: com
ms.assetid: 9411cbed-fa3b-46f7-b677-6ada53324edc
ms.date: 12/05/2018
ms.keywords: CoUninitialize, CoUninitialize function [COM], _com_CoUninitialize, com.couninitialize, combaseapi/CoUninitialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoUninitialize
 - combaseapi/CoUninitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoUninitialize
---

# CoUninitialize function


## -description

Closes the COM library on the current thread, unloads all DLLs loaded by the thread, frees any other resources that the thread maintains, and forces all RPC connections on the thread to close.



## -remarks

A thread must call <b>CoUninitialize</b> once for each successful call it has made to the <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> function, including any call that returns S_FALSE. Only the <b>CoUninitialize</b> call corresponding to the <b>CoInitialize</b> or <b>CoInitializeEx</b> call that initialized the library can close it.



Calls to <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> must be balanced by calls to <a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a>. The <b>OleUninitialize</b> function calls <b>CoUninitialize</b> internally, so applications that call <b>OleUninitialize</b> do not also need to call <b>CoUninitialize</b>.



<b>CoUninitialize</b> should be called on application shutdown, as the last call made to the COM library after the application hides its main windows and falls through its main message loop. If there are open conversations remaining, <b>CoUninitialize</b> starts a modal message loop and dispatches any pending messages from the containers or server for this COM application. By dispatching the messages, <b>CoUninitialize</b> ensures that the application does not quit before receiving all of its pending messages. Non-COM messages are discarded.



Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>, <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, or <b>CoUninitialize</b> from the <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a>
