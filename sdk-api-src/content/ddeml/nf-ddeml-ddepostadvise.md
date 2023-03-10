---
UID: NF:ddeml.DdePostAdvise
title: DdePostAdvise function (ddeml.h)
description: Causes the system to send an XTYP_ADVREQ transaction to the calling (server) application's Dynamic Data Exchange (DDE) callback function for each client with an active advise loop on the specified topic and item.
helpviewer_keywords: ["DdePostAdvise","DdePostAdvise function [Data Exchange]","_win32_DdePostAdvise","_win32_ddepostadvise_cpp","dataxchg.ddepostadvise","ddeml/DdePostAdvise","winui._win32_ddepostadvise"]
old-location: dataxchg\ddepostadvise.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddepostadvise.htm
ms.date: 12/05/2018
ms.keywords: DdePostAdvise, DdePostAdvise function [Data Exchange], _win32_DdePostAdvise, _win32_ddepostadvise_cpp, dataxchg.ddepostadvise, ddeml/DdePostAdvise, winui._win32_ddepostadvise
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
 - DdePostAdvise
 - ddeml/DdePostAdvise
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
 - DdePostAdvise
---

# DdePostAdvise function


## -description

Causes the system to send an <a href="/windows/desktop/dataxchg/xtyp-advreq">XTYP_ADVREQ</a> transaction to the calling (server) application's Dynamic Data Exchange (DDE) callback function for each client with an active advise loop on the specified topic and item. A server application should call this function whenever the data associated with the topic name or item name pair changes.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to a string that specifies the topic name. To send notifications for all topics with active advise loops, an application can set this parameter to 0L.

### -param hszItem [in]

Type: <b>HSZ</b>

A handle to a string that specifies the item name. To send notifications for all items with active advise loops, an application can set this parameter to 0L.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

A server that has nonenumerable topics or items should set the 
				<i>hszTopic</i> and 
				<i>hszItem</i> parameters to <b>NULL</b> so that the system generates transactions for all active advise loops. The server's DDE callback function returns <b>NULL</b> for any advise loops that must not be updated. 

If a server calls <b>DdePostAdvise</b> with a topic, item, and format name set that includes the set currently being handled in an <a href="/windows/desktop/dataxchg/xtyp-advreq">XTYP_ADVREQ</a> callback, a stack overflow can result.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/xtyp-advreq">XTYP_ADVREQ</a>