---
UID: NF:ole2.OleInitialize
title: OleInitialize function (ole2.h)
description: Initializes the COM library on the current apartment, identifies the concurrency model as single-thread apartment (STA), and enables additional functionality described in the Remarks section below.
helpviewer_keywords: ["OleInitialize","OleInitialize function [COM]","_ole_OleInitialize","com.oleinitialize","ole2/OleInitialize"]
old-location: com\oleinitialize.htm
tech.root: com
ms.assetid: 9a13e7a0-f2e2-466b-98f5-38d5972fa391
ms.date: 12/05/2018
ms.keywords: OleInitialize, OleInitialize function [COM], _ole_OleInitialize, com.oleinitialize, ole2/OleInitialize
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleInitialize
 - ole2/OleInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-0.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleInitialize
req.apiset: ext-ms-win-com-ole32-l1-1-0 (introduced in Windows 8)
---

# OleInitialize function


## -description

Initializes the COM library on the current apartment, identifies the concurrency model as single-thread apartment (STA), and enables additional functionality described in the Remarks section below. Applications must initialize the COM library before they can call COM library functions other than <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a> and memory allocation functions.

## -parameters

### -param pvReserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The COM library is already initialized on this apartment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_WRONGCOMPOBJ</b></dt>
</dl>
</td>
<td width="60%">
The versions of COMPOBJ.DLL and OLE2.DLL on your machine are incompatible with each other.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CHANGED_MODE</b></dt>
</dl>
</td>
<td width="60%">
A previous call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> specified the concurrency model for this apartment as multithread apartment (MTA). This could also mean that a change from neutral threaded apartment to single threaded apartment occurred.

</td>
</tr>
</table>

## -remarks

Applications that use the following functionality must call <b>OleInitialize</b> before calling any other function in the COM library: 



<ul>
<li>Clipboard</li>
<li>Drag and Drop</li>
<li>Object linking and embedding (OLE)</li>
<li>In-place activation</li>
</ul>
<b>OleInitialize</b> calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> internally to initialize the COM library on the current apartment. Because OLE operations are not thread-safe, <b>OleInitialize</b> specifies the concurrency model as single-thread apartment.

Once the concurrency model for an apartment is set, it cannot be changed. A call to <b>OleInitialize</b> on an apartment that was previously initialized as multithreaded will fail and return RPC_E_CHANGED_MODE.

You need to initialize the COM library on an apartment before you call any of the library functions except <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>, to get a pointer to the standard allocator, and the memory allocation functions.

Typically, the COM library is initialized on an apartment only once. Subsequent calls will succeed, as long as they do not attempt to change the concurrency model of the apartment, but will return S_FALSE. To close the COM library gracefully, each successful call to <b>OleInitialize</b>, including those that return S_FALSE, must be balanced by a corresponding call to <a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a>.

Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <b>OleInitialize</b> or <a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a> from the <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a>
