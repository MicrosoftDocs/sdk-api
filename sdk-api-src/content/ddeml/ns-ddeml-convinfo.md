---
UID: NS:ddeml.tagCONVINFO
title: CONVINFO (ddeml.h)
description: Contains information about a Dynamic Data Exchange (DDE) conversation.
helpviewer_keywords: ["*PCONVINFO","CONVINFO","CONVINFO structure [Data Exchange]","PCONVINFO","PCONVINFO structure pointer [Data Exchange]","ST_ADVISE","ST_BLOCKED","ST_BLOCKNEXT","ST_CLIENT","ST_CONNECTED","ST_INLIST","ST_ISLOCAL","ST_ISSELF","ST_TERMINATED","XST_ADVACKRCVD","XST_ADVDATAACKRCVD","XST_ADVDATASENT","XST_ADVSENT","XST_CONNECTED","XST_DATARCVD","XST_EXECACKRCVD","XST_EXECSENT","XST_INCOMPLETE","XST_INIT1","XST_INIT2","XST_NULL","XST_POKEACKRCVD","XST_POKESENT","XST_REQSENT","XST_UNADVACKRCVD","XST_UNADVSENT","XTYP_ADVDATA","XTYP_ADVREQ","XTYP_ADVSTART","XTYP_ADVSTOP","XTYP_CONNECT","XTYP_CONNECT_CONFIRM","XTYP_DISCONNECT","XTYP_EXECUTE","XTYP_MONITOR","XTYP_POKE","XTYP_REGISTER","XTYP_REQUEST","XTYP_UNREGISTER","XTYP_WILDCONNECT","XTYP_XACT_COMPLETE","_win32_CONVINFO_str","_win32_convinfo_str_cpp","dataxchg.convinfo_str","ddeml/CONVINFO","ddeml/PCONVINFO","winui._win32_convinfo_str"]
old-location: dataxchg\convinfo_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\convinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PCONVINFO, CONVINFO, CONVINFO structure [Data Exchange], PCONVINFO, PCONVINFO structure pointer [Data Exchange], ST_ADVISE, ST_BLOCKED, ST_BLOCKNEXT, ST_CLIENT, ST_CONNECTED, ST_INLIST, ST_ISLOCAL, ST_ISSELF, ST_TERMINATED, XST_ADVACKRCVD, XST_ADVDATAACKRCVD, XST_ADVDATASENT, XST_ADVSENT, XST_CONNECTED, XST_DATARCVD, XST_EXECACKRCVD, XST_EXECSENT, XST_INCOMPLETE, XST_INIT1, XST_INIT2, XST_NULL, XST_POKEACKRCVD, XST_POKESENT, XST_REQSENT, XST_UNADVACKRCVD, XST_UNADVSENT, XTYP_ADVDATA, XTYP_ADVREQ, XTYP_ADVSTART, XTYP_ADVSTOP, XTYP_CONNECT, XTYP_CONNECT_CONFIRM, XTYP_DISCONNECT, XTYP_EXECUTE, XTYP_MONITOR, XTYP_POKE, XTYP_REGISTER, XTYP_REQUEST, XTYP_UNREGISTER, XTYP_WILDCONNECT, XTYP_XACT_COMPLETE, _win32_CONVINFO_str, _win32_convinfo_str_cpp, dataxchg.convinfo_str, ddeml/CONVINFO, ddeml/PCONVINFO, winui._win32_convinfo_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CONVINFO, *PCONVINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCONVINFO
 - ddeml/tagCONVINFO
 - PCONVINFO
 - ddeml/PCONVINFO
 - CONVINFO
 - ddeml/CONVINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - CONVINFO
---

# CONVINFO structure


## -description

Contains information about a Dynamic Data Exchange (DDE) conversation.

## -struct-fields

### -field cb

Type: <b>DWORD</b>

The structure's size, in bytes.

### -field hUser

Type: <b>DWORD_PTR</b>

Application-defined data.

### -field hConvPartner

Type: <b>HCONV</b>

A handle to the partner application in the DDE conversation. This member is zero if the partner has not registered itself (using the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function) to make DDEML function calls. An application should not pass this member to any DDEML function except <a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a>.

### -field hszSvcPartner

Type: <b>HSZ</b>

A handle to the service name of the partner application.

### -field hszServiceReq

Type: <b>HSZ</b>

A handle to the service name of the server application that was requested for connection.

### -field hszTopic

Type: <b>HSZ</b>

A handle to the name of the requested topic.

### -field hszItem

Type: <b>HSZ</b>

A handle to the name of the requested item. This member is transaction specific.

### -field wFmt

Type: <b>UINT</b>

The format of the data being exchanged. This member is transaction specific.

### -field wType

Type: <b>UINT</b>

The type of the current transaction. This member is transaction specific; it can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XTYP_ADVDATA"></a><a id="xtyp_advdata"></a><dl>
<dt><b>XTYP_ADVDATA</b></dt>
<dt>0x4010</dt>
</dl>
</td>
<td width="60%">
Informs a client that advise data from a server has arrived.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_ADVREQ"></a><a id="xtyp_advreq"></a><dl>
<dt><b>XTYP_ADVREQ</b></dt>
<dt>0x2022</dt>
</dl>
</td>
<td width="60%">
Requests a server to send updated data to the client during an advise loop. This transaction results when the server calls <a href="/windows/desktop/api/ddeml/nf-ddeml-ddepostadvise">DdePostAdvise</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_ADVSTART"></a><a id="xtyp_advstart"></a><dl>
<dt><b>XTYP_ADVSTART</b></dt>
<dt>0x1030</dt>
</dl>
</td>
<td width="60%">
Requests a server to begin an advise loop with a client.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_ADVSTOP"></a><a id="xtyp_advstop"></a><dl>
<dt><b>XTYP_ADVSTOP</b></dt>
<dt>0x8040</dt>
</dl>
</td>
<td width="60%">
Notifies a server that an advise loop is stopping.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_CONNECT"></a><a id="xtyp_connect"></a><dl>
<dt><b>XTYP_CONNECT</b></dt>
<dt>0x1062</dt>
</dl>
</td>
<td width="60%">
Requests a server to establish a conversation with a client.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_CONNECT_CONFIRM"></a><a id="xtyp_connect_confirm"></a><dl>
<dt><b>XTYP_CONNECT_CONFIRM</b></dt>
<dt>0x8072</dt>
</dl>
</td>
<td width="60%">
Notifies a server that a conversation with a client has been established.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_DISCONNECT"></a><a id="xtyp_disconnect"></a><dl>
<dt><b>XTYP_DISCONNECT</b></dt>
<dt>0x80C2</dt>
</dl>
</td>
<td width="60%">
Notifies a server that a conversation has terminated.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_EXECUTE"></a><a id="xtyp_execute"></a><dl>
<dt><b>XTYP_EXECUTE</b></dt>
<dt>0x4050</dt>
</dl>
</td>
<td width="60%">
Requests a server to execute a command sent by a client.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_MONITOR"></a><a id="xtyp_monitor"></a><dl>
<dt><b>XTYP_MONITOR</b></dt>
<dt>0x80F2</dt>
</dl>
</td>
<td width="60%">
Notifies an application registered as <b>APPCMD_MONITOR</b> that DDE data is being transmitted.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_POKE"></a><a id="xtyp_poke"></a><dl>
<dt><b>XTYP_POKE</b></dt>
<dt>0x4090</dt>
</dl>
</td>
<td width="60%">
Requests a server to accept unsolicited data from a client.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_REGISTER"></a><a id="xtyp_register"></a><dl>
<dt><b>XTYP_REGISTER</b></dt>
<dt>0x80A2</dt>
</dl>
</td>
<td width="60%">
Notifies other DDEML applications that a server has registered a service name.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_REQUEST"></a><a id="xtyp_request"></a><dl>
<dt><b>XTYP_REQUEST</b></dt>
<dt>0x20B0</dt>
</dl>
</td>
<td width="60%">
Requests a server to send data to a client.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_UNREGISTER"></a><a id="xtyp_unregister"></a><dl>
<dt><b>XTYP_UNREGISTER</b></dt>
<dt>0x80D2</dt>
</dl>
</td>
<td width="60%">
Notifies other DDEML applications that a server has unregistered a service name.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_WILDCONNECT"></a><a id="xtyp_wildconnect"></a><dl>
<dt><b>XTYP_WILDCONNECT</b></dt>
<dt>0x20E2</dt>
</dl>
</td>
<td width="60%">
Requests a server to establish multiple conversations with the same client.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_XACT_COMPLETE"></a><a id="xtyp_xact_complete"></a><dl>
<dt><b>XTYP_XACT_COMPLETE</b></dt>
<dt>0x8080</dt>
</dl>
</td>
<td width="60%">
Notifies a client that an asynchronous data transaction has been completed.

</td>
</tr>
</table>

### -field wStatus

Type: <b>UINT</b>

The status of the current conversation. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ST_ADVISE"></a><a id="st_advise"></a><dl>
<dt><b>ST_ADVISE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
One or more links are in progress.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_BLOCKED"></a><a id="st_blocked"></a><dl>
<dt><b>ST_BLOCKED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The conversation is blocked.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_BLOCKNEXT"></a><a id="st_blocknext"></a><dl>
<dt><b>ST_BLOCKNEXT</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
The conversation will block after calling the next callback.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_CLIENT"></a><a id="st_client"></a><dl>
<dt><b>ST_CLIENT</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The con0x0010versation handle passed to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a> function is a client-side handle. If the handle is zero, the conversation handle passed to the <b>DdeQueryConvInfo</b> function is a server-side handle.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_CONNECTED"></a><a id="st_connected"></a><dl>
<dt><b>ST_CONNECTED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The conversation is connected.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_INLIST"></a><a id="st_inlist"></a><dl>
<dt><b>ST_INLIST</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The conversation is a member of a conversation list.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_ISLOCAL"></a><a id="st_islocal"></a><dl>
<dt><b>ST_ISLOCAL</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Both sides of the conversation are using the DDEML.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_ISSELF"></a><a id="st_isself"></a><dl>
<dt><b>ST_ISSELF</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Both sides of the conversation are using the same instance of the DDEML.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_TERMINATED"></a><a id="st_terminated"></a><dl>
<dt><b>ST_TERMINATED</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The conversation has been terminated by the partner.

</td>
</tr>
</table>

### -field wConvst

Type: <b>UINT</b>

The conversation state. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XST_ADVACKRCVD"></a><a id="xst_advackrcvd"></a><dl>
<dt><b>XST_ADVACKRCVD</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The advise transaction has just been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_ADVDATAACKRCVD"></a><a id="xst_advdataackrcvd"></a><dl>
<dt><b>XST_ADVDATAACKRCVD</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The advise data transaction has just been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_ADVDATASENT"></a><a id="xst_advdatasent"></a><dl>
<dt><b>XST_ADVDATASENT</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
Advise data has been sent and is awaiting an acknowledgment.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_ADVSENT"></a><a id="xst_advsent"></a><dl>
<dt><b>XST_ADVSENT</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
An advise transaction is awaiting an acknowledgment.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_CONNECTED"></a><a id="xst_connected"></a><dl>
<dt><b>XST_CONNECTED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The conversation has no active transactions.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_DATARCVD"></a><a id="xst_datarcvd"></a><dl>
<dt><b>XST_DATARCVD</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The requested data has just been received.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_EXECACKRCVD"></a><a id="xst_execackrcvd"></a><dl>
<dt><b>XST_EXECACKRCVD</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
An execute transaction has just been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_EXECSENT"></a><a id="xst_execsent"></a><dl>
<dt><b>XST_EXECSENT</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
An execute transaction is awaiting an acknowledgment.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_INCOMPLETE"></a><a id="xst_incomplete"></a><dl>
<dt><b>XST_INCOMPLETE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The last transaction failed.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_INIT1"></a><a id="xst_init1"></a><dl>
<dt><b>XST_INIT1</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Mid-initiate state 1.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_INIT2"></a><a id="xst_init2"></a><dl>
<dt><b>XST_INIT2</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Mid-initiate state 2.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_NULL"></a><a id="xst_null"></a><dl>
<dt><b>XST_NULL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Pre-initiate state.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_POKEACKRCVD"></a><a id="xst_pokeackrcvd"></a><dl>
<dt><b>XST_POKEACKRCVD</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
A poke transaction has just been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_POKESENT"></a><a id="xst_pokesent"></a><dl>
<dt><b>XST_POKESENT</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
A poke transaction is awaiting an acknowledgment.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_REQSENT"></a><a id="xst_reqsent"></a><dl>
<dt><b>XST_REQSENT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
A request transaction is awaiting an acknowledgment.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_UNADVACKRCVD"></a><a id="xst_unadvackrcvd"></a><dl>
<dt><b>XST_UNADVACKRCVD</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
An unadvise transaction has just been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="XST_UNADVSENT"></a><a id="xst_unadvsent"></a><dl>
<dt><b>XST_UNADVSENT</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
An unadvise transaction is awaiting an acknowledgment.

</td>
</tr>
</table>

### -field wLastError

Type: <b>UINT</b>

The error value associated with the last transaction.

### -field hConvList

Type: <b>HCONVLIST</b>

A handle to the conversation list if the handle to the current conversation is in a conversation list. This member is <b>NULL</b> if the conversation is not in a conversation list.

### -field ConvCtxt

Type: <b><a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a></b>

The conversation context.

### -field hwndPartner

Type: <b>HWND</b>

A handle to the window of the partner application involved in the current conversation.

### -field hwnd

Type: <b>HWND</b>

A handle to the window of the calling application involved in the conversation.

## -see-also

<a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddepostadvise">DdePostAdvise</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>