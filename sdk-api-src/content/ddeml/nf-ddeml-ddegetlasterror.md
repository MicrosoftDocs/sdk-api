---
UID: NF:ddeml.DdeGetLastError
title: DdeGetLastError function (ddeml.h)
description: Retrieves the most recent error code set by the failure of a Dynamic Data Exchange Management Library (DDEML) function and resets the error code to DMLERR_NO_ERROR.
helpviewer_keywords: ["DdeGetLastError","DdeGetLastError function [Data Exchange]","_win32_DdeGetLastError","_win32_ddegetlasterror_cpp","dataxchg.ddegetlasterror","ddeml/DdeGetLastError","winui._win32_ddegetlasterror"]
old-location: dataxchg\ddegetlasterror.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddegetlasterror.htm
ms.date: 12/05/2018
ms.keywords: DdeGetLastError, DdeGetLastError function [Data Exchange], _win32_DdeGetLastError, _win32_ddegetlasterror_cpp, dataxchg.ddegetlasterror, ddeml/DdeGetLastError, winui._win32_ddegetlasterror
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
 - DdeGetLastError
 - ddeml/DdeGetLastError
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
 - DdeGetLastError
---

# DdeGetLastError function


## -description

Retrieves the most recent error code set by the failure of a Dynamic Data Exchange Management Library (DDEML) function and resets the error code to DMLERR_NO_ERROR.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value is the last error code, which can be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_ADVACKTIMEOUT</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
A request for a synchronous advise transaction has timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_BUSY</b></dt>
<dt>0x4001</dt>
</dl>
</td>
<td width="60%">
The response to the transaction caused the <b>DDE_FBUSY</b> flag to be set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_DATAACKTIMEOUT</b></dt>
<dt>0x4002</dt>
</dl>
</td>
<td width="60%">
A request for a synchronous data transaction has timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_DLL_NOT_INITIALIZED</b></dt>
<dt>0x4003</dt>
</dl>
</td>
<td width="60%">
A DDEML function was called without first calling the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function, or an invalid instance identifier was passed to a DDEML function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_DLL_USAGE</b></dt>
<dt>0x4004</dt>
</dl>
</td>
<td width="60%">
An application initialized as <b>APPCLASS_MONITOR</b> has attempted to perform a DDE transaction, or an application initialized as <b>APPCMD_CLIENTONLY</b> has attempted to perform server transactions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_EXECACKTIMEOUT</b></dt>
<dt>0x4005</dt>
</dl>
</td>
<td width="60%">
A request for a synchronous execute transaction has timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_INVALIDPARAMETER</b></dt>
<dt>0x4006</dt>
</dl>
</td>
<td width="60%">
A parameter failed to be validated by the DDEML. Some of the possible causes follow: 

The application used a data handle initialized with a different item name handle than was required by the transaction. 

The application used a data handle that was initialized with a different clipboard data format than was required by the transaction. 

The application used a client-side conversation handle with a server-side function or vice versa. 

The application used a freed data handle or string handle. 

More than one instance of the application used the same object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_LOW_MEMORY</b></dt>
<dt>0x4007</dt>
</dl>
</td>
<td width="60%">
A DDEML application has created a prolonged race condition (in which the server application outruns the client), causing large amounts of memory to be consumed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_MEMORY_ERROR</b></dt>
<dt>0x4008</dt>
</dl>
</td>
<td width="60%">
A memory allocation has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_NO_CONV_ESTABLISHED</b></dt>
<dt>0x400a</dt>
</dl>
</td>
<td width="60%">
A client's attempt to establish a conversation has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_NOTPROCESSED</b></dt>
<dt>0x4009</dt>
</dl>
</td>
<td width="60%">
A transaction has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_POKEACKTIMEOUT</b></dt>
<dt>0x400b</dt>
</dl>
</td>
<td width="60%">
A request for a synchronous poke transaction has timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_POSTMSG_FAILED</b></dt>
<dt>0x400c</dt>
</dl>
</td>
<td width="60%">
An internal call to the <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_REENTRANCY</b></dt>
<dt>0x400d</dt>
</dl>
</td>
<td width="60%">
An application instance with a synchronous transaction already in progress attempted to initiate another synchronous transaction, or the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeenablecallback">DdeEnableCallback</a> function was called from within a DDEML callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_SERVER_DIED</b></dt>
<dt>0x400e</dt>
</dl>
</td>
<td width="60%">
A server-side transaction was attempted on a conversation terminated by the client, or the server terminated before completing a transaction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_SYS_ERROR</b></dt>
<dt>0x400f</dt>
</dl>
</td>
<td width="60%">
An internal error has occurred in the DDEML.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_UNADVACKTIMEOUT</b></dt>
<dt>0x4010</dt>
</dl>
</td>
<td width="60%">
A request to end an advise transaction has timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMLERR_UNFOUND_QUEUE_ID</b></dt>
<dt>0x4011</dt>
</dl>
</td>
<td width="60%">
An invalid transaction identifier was passed to a DDEML function. Once the application has returned from an <a href="/windows/desktop/dataxchg/xtyp-xact-complete">XTYP_XACT_COMPLETE</a> callback, the transaction identifier for that callback function is no longer valid.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeenablecallback">DdeEnableCallback</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>



<b>Reference</b>