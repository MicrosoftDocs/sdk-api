---
UID: NF:ddeml.DdeUninitialize
title: DdeUninitialize function (ddeml.h)
description: Frees all Dynamic Data Exchange Management Library (DDEML) resources associated with the calling application.
helpviewer_keywords: ["DdeUninitialize","DdeUninitialize function [Data Exchange]","_win32_DdeUninitialize","_win32_ddeuninitialize_cpp","dataxchg.ddeuninitialize","ddeml/DdeUninitialize","winui._win32_ddeuninitialize"]
old-location: dataxchg\ddeuninitialize.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeuninitialize.htm
ms.date: 12/05/2018
ms.keywords: DdeUninitialize, DdeUninitialize function [Data Exchange], _win32_DdeUninitialize, _win32_ddeuninitialize_cpp, dataxchg.ddeuninitialize, ddeml/DdeUninitialize, winui._win32_ddeuninitialize
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
 - DdeUninitialize
 - ddeml/DdeUninitialize
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
 - DdeUninitialize
---

# DdeUninitialize function


## -description

Frees all Dynamic Data Exchange Management Library (DDEML) resources associated with the calling application.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

<b>DdeUninitialize</b> terminates any conversations currently open for the application.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnect">DdeDisconnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnectlist">DdeDisconnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>