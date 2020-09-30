---
UID: NF:ddeml.DdeEnableCallback
title: DdeEnableCallback function (ddeml.h)
description: Enables or disables transactions for a specific conversation or for all conversations currently established by the calling application.
helpviewer_keywords: ["DdeEnableCallback","DdeEnableCallback function [Data Exchange]","EC_DISABLE","EC_ENABLEALL","EC_ENABLEONE","EC_QUERYWAITING","_win32_DdeEnableCallback","_win32_ddeenablecallback_cpp","dataxchg.ddeenablecallback","ddeml/DdeEnableCallback","winui._win32_ddeenablecallback"]
old-location: dataxchg\ddeenablecallback.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeenablecallback.htm
ms.date: 12/05/2018
ms.keywords: DdeEnableCallback, DdeEnableCallback function [Data Exchange], EC_DISABLE, EC_ENABLEALL, EC_ENABLEONE, EC_QUERYWAITING, _win32_DdeEnableCallback, _win32_ddeenablecallback_cpp, dataxchg.ddeenablecallback, ddeml/DdeEnableCallback, winui._win32_ddeenablecallback
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
 - DdeEnableCallback
 - ddeml/DdeEnableCallback
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
 - DdeEnableCallback
---

# DdeEnableCallback function


## -description

Enables or disables transactions for a specific conversation or for all conversations currently established by the calling application.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application-instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation to enable or disable. If this parameter is <b>NULL</b>, the function affects all conversations.

### -param wCmd [in]

Type: <b>UINT</b>

The function code. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EC_ENABLEALL"></a><a id="ec_enableall"></a><dl>
<dt><b>EC_ENABLEALL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Enables all transactions for the specified conversation.

</td>
</tr>
<tr>
<td width="40%"><a id="EC_ENABLEONE"></a><a id="ec_enableone"></a><dl>
<dt><b>EC_ENABLEONE</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Enables one transaction for the specified conversation.

</td>
</tr>
<tr>
<td width="40%"><a id="EC_DISABLE"></a><a id="ec_disable"></a><dl>
<dt><b>EC_DISABLE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Disables all blockable transactions for the specified conversation. 

A server application can disable the following transactions:

<ul>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advstart">XTYP_ADVSTART</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advstop">XTYP_ADVSTOP</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-execute">XTYP_EXECUTE</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-poke">XTYP_POKE</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-request">XTYP_REQUEST</a>
</li>
</ul>
A client application can disable the following transactions:

<ul>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advdata">XTYP_ADVDATA</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-xact-complete">XTYP_XACT_COMPLETE</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EC_QUERYWAITING"></a><a id="ec_querywaiting"></a><dl>
<dt><b>EC_QUERYWAITING</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Determines whether any transactions are in the queue for the specified conversation.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

If the 
						<i>wCmd</i> parameter is <b>EC_QUERYWAITING</b>, and the application transaction queue contains one or more unprocessed transactions that are not being processed, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>.

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

An application can disable transactions for a specific conversation by returning the <b>CBR_BLOCK</b> return code from its Dynamic Data Exchange (DDE) callback function. When you reenable the conversation by using the <b>DdeEnableCallback</b> function, the operating system generates the same transaction that was in process when the conversation was disabled. 

Using the <b>EC_QUERYWAITING</b> flag does not change the enable state of the conversation and does not cause transactions to be issued within the context of the call to <b>DdeEnableCallback</b>. 

If <b>DdeEnableCallback</b> is called with <b>EC_QUERYWAITING</b> and the function returns a nonzero, an application should try to quickly allow message processing, return from its callback, or enable callbacks. Such a result does not guarantee that subsequent callbacks will be made. Calling <b>DdeEnableCallback</b> with <b>EC_QUERYWAITING</b> lets an application with blocked callbacks determine whether there are any transactions pending on the blocked conversation. Of course, even if such a call returns zero, an application should always process messages in a timely manner.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddedisconnect">DdeDisconnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>