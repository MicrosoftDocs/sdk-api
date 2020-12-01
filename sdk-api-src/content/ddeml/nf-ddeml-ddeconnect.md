---
UID: NF:ddeml.DdeConnect
title: DdeConnect function (ddeml.h)
description: Establishes a conversation with a server application that supports the specified service name and topic name pair. If more than one such server exists, the system selects only one.
helpviewer_keywords: ["DdeConnect","DdeConnect function [Data Exchange]","_win32_DdeConnect","_win32_ddeconnect_cpp","dataxchg.ddeconnect","ddeml/DdeConnect","winui._win32_ddeconnect"]
old-location: dataxchg\ddeconnect.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeconnect.htm
ms.date: 12/05/2018
ms.keywords: DdeConnect, DdeConnect function [Data Exchange], _win32_DdeConnect, _win32_ddeconnect_cpp, dataxchg.ddeconnect, ddeml/DdeConnect, winui._win32_ddeconnect
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
 - DdeConnect
 - ddeml/DdeConnect
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
 - DdeConnect
---

# DdeConnect function


## -description

Establishes a conversation with a server application that supports the specified service name and topic name pair. If more than one such server exists, the system selects only one.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hszService [in]

Type: <b>HSZ</b>

A handle to the string that specifies the service name of the server application with which a conversation is to be established. This handle must have been created by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a> function. If this parameter is 0L, a conversation is established with any available server.

### -param hszTopic [in]

Type: <b>HSZ</b>

A handle to the string that specifies the name of the topic on which a conversation is to be established. This handle must have been created by a previous call to <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a>. If this parameter is 0L, a conversation on any topic supported by the selected server is established.

### -param pCC [in, optional]

Type: <b>PCONVCONTEXT</b>

A pointer to the <a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a> structure that contains conversation context information. If this parameter is <b>NULL</b>, the server receives the default <b>CONVCONTEXT</b> structure during the 
					<a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a> or 
					<a href="/windows/desktop/dataxchg/xtyp-wildconnect">XTYP_WILDCONNECT</a> transaction.

## -returns

Type: <b>HCONV</b>

If the function succeeds, the return value is the handle to the established conversation.

If the function fails, the return value is 0L. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

The client application cannot make assumptions regarding the server selected. If an instance-specific name is specified in the 
				<i>hszService</i> parameter, a conversation is established with only the specified instance. Instance-specific service names are passed to an application's Dynamic Data Exchange (DDE) callback function during the <a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a> and <a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a> transactions. 

All members of the default <a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a> structure are set to zero except 
				<i>cb</i>, which specifies the size of the structure, and 
				<i>iCodePage</i>, which specifies <b>CP_WINANSI</b> (the default code page) or <b>CP_WINUNICODE</b>, depending on whether the ANSI or Unicode version of the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function was called by the client application.

## -see-also

<a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnect">DdeDisconnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnectlist">DdeDisconnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a>



<a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a>