---
UID: NF:roapi.RoUninitialize
title: RoUninitialize function (roapi.h)
description: Closes the Windows Runtime on the current thread.
helpviewer_keywords: ["RoUninitialize","RoUninitialize function [Windows Runtime]","WinRTUninitialize","roapi/RoUninitialize","roapi/WinRTUninitialize","winrt.rouninitialize","winrt.winrtuninitialize"]
old-location: winrt\rouninitialize.htm
tech.root: WinRT
ms.assetid: 0F910E71-BA44-44A6-8432-52A4E38854F9
ms.date: 12/05/2018
ms.keywords: RoUninitialize, RoUninitialize function [Windows Runtime], WinRTUninitialize, roapi/RoUninitialize, roapi/WinRTUninitialize, winrt.rouninitialize, winrt.winrtuninitialize
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoUninitialize
 - roapi/RoUninitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roapi.h
 - API-MS-Win-Core-WinRT-l1-1-0.dll
 - ComBase.dll
 - api-ms-win-core-winrt-string-l1-1-0.dll
api_name:
 - RoUninitialize
 - WinRTUninitialize
---

# RoUninitialize function


## -description

Closes the Windows Runtime on the current thread.



## -remarks

Call the <b>RoUninitialize</b> function to close the Windows Runtime on the current thread. This unloads all DLLs loaded by the thread, frees any other resources that the thread maintains, and forces all RPC connections on the thread to close.

Use the <a href="/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a> function to initialize a thread in the Windows Runtime.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>



<a href="/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a>
