---
UID: NC:ddeml.PFNCALLBACK
title: PFNCALLBACK (ddeml.h)
description: An application-defined callback function used with the Dynamic Data Exchange Management Library (DDEML) functions.
helpviewer_keywords: ["PFNCALLBACK","PFNCALLBACK callback","PFNCALLBACK callback function [Data Exchange]","XCLASS_BOOL","XCLASS_DATA","XCLASS_FLAGS","XCLASS_NOTIFICATION","_win32_DdeCallback","_win32_ddecallback_cpp","dataxchg.ddecallback","ddeml/PFNCALLBACK","winui._win32_ddecallback"]
old-location: dataxchg\ddecallback.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecallback.htm
ms.date: 12/05/2018
ms.keywords: PFNCALLBACK, PFNCALLBACK callback, PFNCALLBACK callback function [Data Exchange], XCLASS_BOOL, XCLASS_DATA, XCLASS_FLAGS, XCLASS_NOTIFICATION, _win32_DdeCallback, _win32_ddecallback_cpp, dataxchg.ddecallback, ddeml/PFNCALLBACK, winui._win32_ddecallback
f1_keywords:
- ddeml/PFNCALLBACK
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ddeml.h
api_name:
- PFNCALLBACK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

An application-defined callback function used with the <a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a> (DDEML) functions. It processes Dynamic Data Exchange (DDE) transactions. The 
			<b>PFNCALLBACK</b> type defines a pointer to this callback function. <i>DdeCallback</i> is a placeholder for the application-defined function name. 

## -parameters

### -param wType [in]

Type: <b>UINT</b>

The type of the current transaction. This parameter consists of a combination of transaction class flags and transaction type flags. The following table describes each of the transaction classes and provides a list of the transaction types in each class. For information about a specific transaction type, see the individual description of that type in **Remarks**.

### -param wFmt [in]

Type: <b>UINT</b>

The format in which data is sent or received. 

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation associated with the current transaction. 

### -param hsz1 [in]

Type: <b>HSZ</b>

A handle to a string. The meaning of this parameter depends on the type of the current transaction. For the meaning of this parameter, see the description of the transaction type in **Remarks**. 

### -param hsz2 [in]

Type: <b>HSZ</b>

A handle to a string. The meaning of this parameter depends on the type of the current transaction. For the meaning of this parameter, see the description of the transaction type in **Remarks**. 

### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to DDE data. The meaning of this parameter depends on the type of the current transaction. For the meaning of this parameter, see the description of the transaction type in **Remarks**.

### -param dwData1 [in]

Type: <b>ULONG_PTR</b>

Transaction-specific data. For the meaning of this parameter, see the description of the transaction type in **Remarks**. 

### -param dwData2 [in]

Type: <b>ULONG_PTR</b>

Transaction-specific data. For the meaning of this parameter, see the description of the transaction type in **Remarks**. 

## -returns

Type: <b>HDDEDATA</b>

The return value depends on the transaction class. For more information about the return values, see descriptions of the individual transaction types. 

## -remarks

### XCLASS_BOOL

A DDE callback function should return <b>TRUE</b> or <b>FALSE</b> when it finishes processing a transaction that belongs to this class. The <b>XCLASS_BOOL</b> transaction class consists of the following types: 

<ul>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advstart">XTYP_ADVSTART</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-connect">XTYP_CONNECT</a>
</li>
</ul>

### XCLASS_DATA

A DDE callback function should return a DDE handle, the <b>CBR_BLOCK</b> return code, or <b>NULL</b> when it finishes processing a transaction that belongs to this class. The <b>XCLASS_DATA</b> transaction class consists of the following types: 

<ul>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advreq">XTYP_ADVREQ</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-request">XTYP_REQUEST</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-wildconnect">XTYP_WILDCONNECT</a>
</li>
</ul>

### XCLASS_FLAGS

A DDE callback function should return <b>DDE_FACK</b>, <b>DDE_FBUSY</b>, or <b>DDE_FNOTPROCESSED</b> when it finishes processing a transaction that belongs to this class. The <b>XCLASS_FLAGS</b> transaction class consists of the following types:

<ul>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advdata">XTYP_ADVDATA</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-execute">XTYP_EXECUTE</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-poke">XTYP_POKE</a>
</li>
</ul>

### XCLASS_NOTIFICATION

The transaction types that belong to this class are for notification purposes only. The return value from the callback function is ignored. The <b>XCLASS_NOTIFICATION</b> transaction class consists of the following types: 

<ul>
<li>
<a href="/windows/desktop/dataxchg/xtyp-advstop">XTYP_ADVSTOP</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-connect-confirm">XTYP_CONNECT_CONFIRM</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-disconnect">XTYP_DISCONNECT</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-error">XTYP_ERROR</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-monitor">XTYP_MONITOR</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-register">XTYP_REGISTER</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-xact-complete">XTYP_XACT_COMPLETE</a>
</li>
<li>
<a href="/windows/desktop/dataxchg/xtyp-unregister">XTYP_UNREGISTER</a>
</li>
</ul>

The callback function is called asynchronously for transactions that do not involve the creation or termination of conversations. An application that does not frequently accept incoming messages will have reduced DDE performance because the Dynamic Data Exchange Management Library (DDEML) uses messages to initiate transactions. 

An application must register the callback function by specifying a pointer to the function in a call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function. 

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeenablecallback">DdeEnableCallback</a>

<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>

<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>