---
UID: NF:ddeml.DdeNameService
title: DdeNameService function (ddeml.h)
description: Registers or unregisters the service names a Dynamic Data Exchange (DDE) server supports.
helpviewer_keywords: ["DNS_FILTEROFF","DNS_FILTERON","DNS_REGISTER","DNS_UNREGISTER","DdeNameService","DdeNameService function [Data Exchange]","_win32_DdeNameService","_win32_ddenameservice_cpp","dataxchg.ddenameservice","ddeml/DdeNameService","winui._win32_ddenameservice"]
old-location: dataxchg\ddenameservice.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddenameservice.htm
ms.date: 12/05/2018
ms.keywords: DNS_FILTEROFF, DNS_FILTERON, DNS_REGISTER, DNS_UNREGISTER, DdeNameService, DdeNameService function [Data Exchange], _win32_DdeNameService, _win32_ddenameservice_cpp, dataxchg.ddenameservice, ddeml/DdeNameService, winui._win32_ddenameservice
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
 - DdeNameService
 - ddeml/DdeNameService
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
 - DdeNameService
---

# DdeNameService function


## -description

Registers or unregisters the service names a Dynamic Data Exchange (DDE) server supports. This function causes the system to send <a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a> or <a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a> transactions to other running <a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a> (DDEML) client applications.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hsz1 [in, optional]

Type: <b>HSZ</b>

A handle to the string that specifies the service name the server is registering or unregistering. An application that is unregistering all of its service names should set this parameter to 0L.

### -param hsz2 [in, optional]

Type: <b>HSZ</b>

Reserved; should be set to 0L.

### -param afCmd [in]

Type: <b>UINT</b>

The service name options. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DNS_REGISTER"></a><a id="dns_register"></a><dl>
<dt><b>DNS_REGISTER</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Registers the error code service name.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_UNREGISTER"></a><a id="dns_unregister"></a><dl>
<dt><b>DNS_UNREGISTER</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Unregisters the error code service name. If the 
						<i>hsz1</i> parameter is 0L, all service names registered by the server will be unregistered.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_FILTERON"></a><a id="dns_filteron"></a><dl>
<dt><b>DNS_FILTERON</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Turns on service name initiation filtering. The filter prevents a server from receiving <a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a> transactions for service names it has not registered. This is the default setting for this filter. 

If a server application does not register any service names, the application cannot receive <a href="/windows/desktop/dataxchg/xtyp-wildconnect">XTYP_WILDCONNECT</a> transactions.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_FILTEROFF"></a><a id="dns_filteroff"></a><dl>
<dt><b>DNS_FILTEROFF</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Turns off service name initiation filtering. If this flag is specified, the server receives an 
						<a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a> transaction whenever another DDE application calls the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a> function, regardless of the service name.

</td>
</tr>
</table>

## -returns

Type: <b>HDDEDATA</b>

If the function succeeds, it returns a nonzero value. That value is not a true <b>HDDEDATA</b> value, merely a Boolean indicator of success. The function is typed <b>HDDEDATA</b> to allow for possible future expansion of the function and a more sophisticated return value. 

If the function fails, the return value is 0L. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

The service name identified by the 
				<i>hsz1</i> parameter should be a base name (that is, the name should contain no instance-specific information). The system generates an instance-specific name and sends it along with the base name during the 
				<a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a> and 
				<a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a> transactions. The receiving applications can then connect to the specific application instance.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a>



<a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a>