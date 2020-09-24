---
UID: NF:ddeml.DdeKeepStringHandle
title: DdeKeepStringHandle function (ddeml.h)
description: Increments the usage count associated with the specified handle.
helpviewer_keywords: ["DdeKeepStringHandle","DdeKeepStringHandle function [Data Exchange]","_win32_DdeKeepStringHandle","_win32_ddekeepstringhandle_cpp","dataxchg.ddekeepstringhandle","ddeml/DdeKeepStringHandle","winui._win32_ddekeepstringhandle"]
old-location: dataxchg\ddekeepstringhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddekeepstringhandle.htm
ms.date: 12/05/2018
ms.keywords: DdeKeepStringHandle, DdeKeepStringHandle function [Data Exchange], _win32_DdeKeepStringHandle, _win32_ddekeepstringhandle_cpp, dataxchg.ddekeepstringhandle, ddeml/DdeKeepStringHandle, winui._win32_ddekeepstringhandle
req.header: ddeml.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeKeepStringHandle
 - ddeml/DdeKeepStringHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeKeepStringHandle
---

# DdeKeepStringHandle function


## -description

Increments the usage count associated with the specified handle. This function enables an application to save a string handle passed to the application's Dynamic Data Exchange (DDE) callback function. Otherwise, a string handle passed to the callback function is deleted when the callback function returns. This function should also be used to keep a copy of a string handle referenced by the <a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a> structure returned by the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a> function.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string handle to be saved.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -see-also

<a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreestringhandle">DdeFreeStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequerystringa">DdeQueryString</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>