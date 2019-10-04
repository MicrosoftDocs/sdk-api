---
UID: NF:roapi.RoInitialize
title: RoInitialize function (roapi.h)
author: windows-sdk-content
description: Initializes the Windows Runtime on the current thread with the specified concurrency model.
old-location: winrt\roinitialize.htm
tech.root: WinRT
ms.assetid: 527A7FF7-749D-4178-A397-5C538F6031F8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RoInitialize, RoInitialize function [Windows Runtime], WinRTInitialize, roapi/RoInitialize, roapi/WinRTInitialize, winrt.roinitialize, winrt.winrtinitialize
ms.topic: function
f1_keywords: 
 - "roapi/RoInitialize"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - roapi.h
 - API-MS-Win-Core-WinRT-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoInitialize
 - WinRTInitialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RoInitialize function


## -description


Initializes the Windows Runtime on the current thread with the specified concurrency model.


## -parameters




### -param initType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/roapi/ne-roapi-ro_init_type">RO_INIT_TYPE</a></b>

The concurrency model for the thread. The default is <b>RO_INIT_MULTITHREADED</b>.


## -returns



Type: <b>HRESULT</b>

This function can return the standard return values <b>E_INVALIDARG</b>, <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The Windows Runtime was initialized successfully on this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The Windows Runtime is already initialized on this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CHANGED_MODE</b></dt>
</dl>
</td>
<td width="60%">
A previous call to <a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a> specified the concurrency model for this thread as multithread apartment (MTA). This could also indicate that a change from neutral-threaded apartment to single-threaded apartment has occurred.

</td>
</tr>
</table>
 




## -remarks



Use the <b>RoInitialize</b> function to initialize a thread in the Windows Runtime. All threads that activate and interact with Windows Runtime objects must be initialized prior to calling into the Windows Runtime. 

Call the <a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-rouninitialize">RoUninitialize</a> function to close the Windows Runtime on the current thread. Each successful call to <b>RoInitialize</b>, including those that return <b>S_FALSE</b>, must be balanced by a corresponding call to <b>RoUninitialize</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roapi/ne-roapi-ro_init_type">RO_INIT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-rouninitialize">RoUninitialize</a>
 

 

