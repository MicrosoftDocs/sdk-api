---
UID: NF:ddeml.DdeAbandonTransaction
title: DdeAbandonTransaction function (ddeml.h)
description: Abandons the specified asynchronous transaction and releases all resources associated with the transaction.
helpviewer_keywords: ["DdeAbandonTransaction","DdeAbandonTransaction function [Data Exchange]","_win32_DdeAbandonTransaction","_win32_ddeabandontransaction_cpp","dataxchg.ddeabandontransaction","ddeml/DdeAbandonTransaction","winui._win32_ddeabandontransaction"]
old-location: dataxchg\ddeabandontransaction.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeabandontransaction.htm
ms.date: 12/05/2018
ms.keywords: DdeAbandonTransaction, DdeAbandonTransaction function [Data Exchange], _win32_DdeAbandonTransaction, _win32_ddeabandontransaction_cpp, dataxchg.ddeabandontransaction, ddeml/DdeAbandonTransaction, winui._win32_ddeabandontransaction
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
 - DdeAbandonTransaction
 - ddeml/DdeAbandonTransaction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-dde-l1-1-0.dll
 - User32.dll
api_name:
 - DdeAbandonTransaction
---

# DdeAbandonTransaction function


## -description

Abandons the specified asynchronous transaction and releases all resources associated with the transaction.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation in which the transaction was initiated. If this parameter is 0L, all transactions are abandoned (that is, the 
					<i>idTransaction</i> parameter is ignored).

### -param idTransaction [in]

Type: <b>DWORD</b>

The identifier of the transaction to be abandoned. If this parameter is 0L, all active transactions in the specified conversation are abandoned.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

Only a Dynamic Data Exchange (DDE) client application should call <b>DdeAbandonTransaction</b>. If the server application responds to the transaction after the client has called <b>DdeAbandonTransaction</b>, the system discards the transaction results. This function has no effect on synchronous transactions.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeclienttransaction">DdeClientTransaction</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>