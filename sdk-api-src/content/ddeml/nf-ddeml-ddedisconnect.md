---
UID: NF:ddeml.DdeDisconnect
title: DdeDisconnect function (ddeml.h)
description: Terminates a conversation started by either the DdeConnect or DdeConnectList function and invalidates the specified conversation handle.
helpviewer_keywords: ["DdeDisconnect","DdeDisconnect function [Data Exchange]","_win32_DdeDisconnect","_win32_ddedisconnect_cpp","dataxchg.ddedisconnect","ddeml/DdeDisconnect","winui._win32_ddedisconnect"]
old-location: dataxchg\ddedisconnect.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddedisconnect.htm
ms.date: 12/05/2018
ms.keywords: DdeDisconnect, DdeDisconnect function [Data Exchange], _win32_DdeDisconnect, _win32_ddedisconnect_cpp, dataxchg.ddedisconnect, ddeml/DdeDisconnect, winui._win32_ddedisconnect
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
 - DdeDisconnect
 - ddeml/DdeDisconnect
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
 - DdeDisconnect
---

# DdeDisconnect function


## -description

Terminates a conversation started by either the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a> or <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a> function and invalidates the specified conversation handle.

## -parameters

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the active conversation to be terminated.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

Any incomplete transactions started before calling <b>DdeDisconnect</b> are immediately abandoned. The <a href="/windows/desktop/dataxchg/xtyp-disconnect">XTYP_DISCONNECT</a> transaction is sent to the Dynamic Data Exchange (DDE) callback function of the partner in the conversation. Generally, only client applications must terminate conversations.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnectlist">DdeDisconnectList</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/xtyp-disconnect">XTYP_DISCONNECT</a>