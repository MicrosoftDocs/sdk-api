---
UID: NF:ole2.OleUninitialize
title: OleUninitialize function (ole2.h)
description: Closes the COM library on the apartment, releases any class factories, other COM objects, or servers held by the apartment, disables RPC on the apartment, and frees any resources the apartment maintains.
helpviewer_keywords: ["OleUninitialize","OleUninitialize function [COM]","_ole_OleUninitialize","com.oleuninitialize","ole2/OleUninitialize"]
old-location: com\oleuninitialize.htm
tech.root: com
ms.assetid: b2a8233f-7e1b-4c54-9363-7478c40c3830
ms.date: 12/05/2018
ms.keywords: OleUninitialize, OleUninitialize function [COM], _ole_OleUninitialize, com.oleuninitialize, ole2/OleUninitialize
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
 - OleUninitialize
 - ole2/OleUninitialize
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
 - OleUninitialize
req.apiset: ext-ms-win-com-ole32-l1-1-0 (introduced in Windows 8)
---

# OleUninitialize function


## -description

Closes the COM library on the apartment, releases any class factories, other COM objects, or servers held by the apartment, disables RPC on the apartment, and frees any resources the apartment maintains.



## -remarks

Call <b>OleUninitialize</b> on application shutdown, as the last COM library call, if the apartment was initialized with a call to <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a>. <b>OleUninitialize</b> calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> function internally to shut down the OLE Component Object(COM) Library.

If the COM library was initialized on the apartment with a call to <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, it must be closed with a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>.

The <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> and <b>OleUninitialize</b> calls must be balanced. If there are multiple calls to the <b>OleInitialize</b> function, there must be the same number of calls to <b>OleUninitialize</b>; only the <b>OleUninitialize</b> call corresponding to the <b>OleInitialize</b> call that actually initialized the library can close it.

Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> or <b>OleUninitialize</b> from the <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleuninitialize">OleUninitialize</a>
