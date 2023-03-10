---
UID: NF:ddeml.DdeReconnect
title: DdeReconnect function (ddeml.h)
description: Enables a client Dynamic Data Exchange Management Library (DDEML) application to attempt to reestablish a conversation with a service that has terminated a conversation with the client.
helpviewer_keywords: ["DdeReconnect","DdeReconnect function [Data Exchange]","_win32_DdeReconnect","_win32_ddereconnect_cpp","dataxchg.ddereconnect","ddeml/DdeReconnect","winui._win32_ddereconnect"]
old-location: dataxchg\ddereconnect.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddereconnect.htm
ms.date: 12/05/2018
ms.keywords: DdeReconnect, DdeReconnect function [Data Exchange], _win32_DdeReconnect, _win32_ddereconnect_cpp, dataxchg.ddereconnect, ddeml/DdeReconnect, winui._win32_ddereconnect
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
 - DdeReconnect
 - ddeml/DdeReconnect
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
 - DdeReconnect
---

# DdeReconnect function


## -description

Enables a client <a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a> (DDEML) application to attempt to reestablish a conversation with a service that has terminated a conversation with the client. When the conversation is reestablished, the Dynamic Data Exchange Management Library (DDEML) attempts to reestablish any preexisting advise loops.

## -parameters

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation to be reestablished. A client must have obtained the conversation handle by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a> function or from an <a href="/windows/desktop/dataxchg/xtyp-disconnect">XTYP_DISCONNECT</a> transaction.

## -returns

Type: <b>HCONV</b>

If the function succeeds, the return value is the handle to the reestablished conversation.

If the function fails, the return value is 0L. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnect">DdeDisconnect</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>