---
UID: NF:ddeml.DdeClientTransaction
title: DdeClientTransaction function
author: windows-sdk-content
description: Begins a data transaction between a client and a server. Only a Dynamic Data Exchange (DDE) client application can call this function, and the application can use it only after establishing a conversation with the server.
old-location: dataxchg\ddeclienttransaction.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeclienttransaction.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DdeClientTransaction, DdeClientTransaction function [Data Exchange], XTYP_ADVSTART, XTYP_ADVSTOP, XTYP_EXECUTE, XTYP_POKE, XTYP_REQUEST, _win32_DdeClientTransaction, _win32_ddeclienttransaction_cpp, dataxchg.ddeclienttransaction, ddeml/DdeClientTransaction, winui._win32_ddeclienttransaction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeClientTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeClientTransaction function


## -description


Begins a data transaction between a client and a server. Only a Dynamic Data Exchange (DDE) client application can call this function, and the application can use it only after establishing a conversation with the server. 


## -parameters




### -param pData [in, optional]

Type: <b>LPBYTE</b>

The beginning of the data the client must pass to the server. 

Optionally, an application can specify the data handle (<b>HDDEDATA</b>) to pass to the server and in that case the 
						<i>cbData</i> parameter should be set to -1. This parameter is required only if the 
						<i>wType</i> parameter is <a href="https://msdn.microsoft.com/6001eb7d-59c0-49ec-97ce-26132891188c">XTYP_EXECUTE</a> or <a href="https://msdn.microsoft.com/63c6115e-24f8-4f35-8397-8be63110b21f">XTYP_POKE</a>. Otherwise, this parameter should be <b>NULL</b>. 

For the optional usage of this parameter, <a href="https://msdn.microsoft.com/63c6115e-24f8-4f35-8397-8be63110b21f">XTYP_POKE</a> transactions where 
						<i>pData</i> is a data handle, the handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a> function, employing the same data format specified in the 
						<i>wFmt</i> parameter. 


### -param cbData [in]

Type: <b>DWORD</b>

The length, in bytes, of the data pointed to by the 
					<i>pData</i> parameter, including the terminating <b>NULL</b>, if the data is a string. A value of -1 indicates that 
					<i>pData</i> is a data handle that identifies the data being sent. 


### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation in which the transaction is to take place. 


### -param hszItem [in, optional]

Type: <b>HSZ</b>

A handle to the data item for which data is being exchanged during the transaction. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function. This parameter is ignored (and should be set to 0L) if the 
					<i>wType</i> parameter is 
					<a href="https://msdn.microsoft.com/6001eb7d-59c0-49ec-97ce-26132891188c">XTYP_EXECUTE</a>. 


### -param wFmt [in]

Type: <b>UINT</b>

The standard clipboard format in which the data item is being submitted or requested. 

If the transaction specified by the <i>wType</i> parameter does not pass data or is 
						<a href="https://msdn.microsoft.com/6001eb7d-59c0-49ec-97ce-26132891188c">XTYP_EXECUTE</a>, this parameter should be zero. 

If the transaction specified by the 
						<i>wType</i> parameter references non-execute DDE data (
						<a href="https://msdn.microsoft.com/63c6115e-24f8-4f35-8397-8be63110b21f">XTYP_POKE</a>, <a href="https://msdn.microsoft.com/8911e722-5656-4ca6-8b0a-6bdf8281611a">XTYP_ADVSTART</a>, <a href="https://msdn.microsoft.com/67dfa463-6a44-43a5-93be-a39c19c87c1c">XTYP_ADVSTOP</a>, 
						<a href="https://msdn.microsoft.com/e776b995-6a64-4398-9e29-c151f3ef4c1d">XTYP_REQUEST</a>), the 
						<i>wFmt</i> value must be either a valid predefined (CF_) DDE format or a valid registered clipboard format. 


### -param wType [in]

Type: <b>UINT</b>

The transaction type. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XTYP_ADVSTART"></a><a id="xtyp_advstart"></a><dl>
<dt><b>XTYP_ADVSTART</b></dt>
<dt>0x1030</dt>
</dl>
</td>
<td width="60%">
Begins an advise loop. Any number of distinct advise loops can exist within a conversation. An application can alter the advise loop type by combining the <a href="https://msdn.microsoft.com/8911e722-5656-4ca6-8b0a-6bdf8281611a">XTYP_ADVSTART</a> transaction type with one or more of the following flags:

<ul>
<li><b>XTYPF_NODATA</b>. Instructs the server to notify the client of any data changes without actually sending the data. This flag gives the client the option of ignoring the notification or requesting the changed data from the server.</li>
<li><b>XTYPF_ACKREQ</b>. Instructs the server to wait until the client acknowledges that it received the previous data item before sending the next data item. This flag prevents a fast server from sending data faster than the client can process it.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_ADVSTOP"></a><a id="xtyp_advstop"></a><dl>
<dt><b>XTYP_ADVSTOP</b></dt>
<dt>0x8040</dt>
</dl>
</td>
<td width="60%">
Ends an advise loop.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_EXECUTE"></a><a id="xtyp_execute"></a><dl>
<dt><b>XTYP_EXECUTE</b></dt>
<dt>0x4050</dt>
</dl>
</td>
<td width="60%">
Begins an execute transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_POKE"></a><a id="xtyp_poke"></a><dl>
<dt><b>XTYP_POKE</b></dt>
<dt>0x4090</dt>
</dl>
</td>
<td width="60%">
Begins a poke transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="XTYP_REQUEST"></a><a id="xtyp_request"></a><dl>
<dt><b>XTYP_REQUEST</b></dt>
<dt>0x20B0</dt>
</dl>
</td>
<td width="60%">
Begins a request transaction.

</td>
</tr>
</table>
 


### -param dwTimeout [in]

Type: <b>DWORD</b>

The maximum amount of time, in milliseconds, that the client will wait for a response from the server application in a synchronous transaction. This parameter should be <b>TIMEOUT_ASYNC</b> for asynchronous transactions. 


### -param pdwResult [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that receives the result of the transaction. An application that does not check the result can use <b>NULL</b> for this value. For synchronous transactions, the low-order word of this variable contains any applicable DDE_ flags resulting from the transaction. This provides support for applications dependent on <b>DDE_APPSTATUS</b> bits. It is, however, recommended that applications no longer use these bits because they may not be supported in future versions of the <a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a> (DDEML). For asynchronous transactions, this variable is filled with a unique transaction identifier for use with the <a href="https://msdn.microsoft.com/d48ed230-7549-408e-b936-3046abeb7d94">DdeAbandonTransaction</a> function and the <a href="https://msdn.microsoft.com/d34a6fab-0e3c-44fe-b25f-7011228fe261">XTYP_XACT_COMPLETE</a> transaction. 


## -returns



Type: <b>HDDEDATA</b>

If the function succeeds, the return value is a data handle that identifies the data for successful synchronous transactions in which the client expects data from the server. The return value is nonzero for successful asynchronous transactions and for synchronous transactions in which the client does not expect data. The return value is zero for all unsuccessful transactions. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



When an application has finished using the data handle returned by <b>DdeClientTransaction</b>, the application should free the handle by calling the <a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a> function. 

Transactions can be synchronous or asynchronous. During a synchronous transaction, <b>DdeClientTransaction</b> does not return until the transaction either completes successfully or fails. Synchronous transactions cause a client to enter a modal loop while waiting for various asynchronous events. Because of this, a client application can still respond to user input while waiting on a synchronous transaction, but the application cannot begin a second synchronous transaction because of the activity associated with the first. <b>DdeClientTransaction</b> fails if any instance of the same task has a synchronous transaction already in progress. 

During an asynchronous transaction, <b>DdeClientTransaction</b> returns after the transaction has begun, passing a transaction identifier for reference. When the server's DDE callback function finishes processing an asynchronous transaction, the system sends an 
				<a href="https://msdn.microsoft.com/d34a6fab-0e3c-44fe-b25f-7011228fe261">XTYP_XACT_COMPLETE</a> transaction to the client. This transaction provides the client with the results of the asynchronous transaction that it initiated by calling <b>DdeClientTransaction</b>. A client application can choose to abandon an asynchronous transaction by calling the <a href="https://msdn.microsoft.com/d48ed230-7549-408e-b936-3046abeb7d94">DdeAbandonTransaction</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d48ed230-7549-408e-b936-3046abeb7d94">DdeAbandonTransaction</a>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a>



<a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a>



<a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/817a6c2a-57e8-4a6d-86db-0c34cfa44999">DdeFreeDataHandle</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8911e722-5656-4ca6-8b0a-6bdf8281611a">XTYP_ADVSTART</a>



<a href="https://msdn.microsoft.com/67dfa463-6a44-43a5-93be-a39c19c87c1c">XTYP_ADVSTOP</a>



<a href="https://msdn.microsoft.com/6001eb7d-59c0-49ec-97ce-26132891188c">XTYP_EXECUTE</a>



<a href="https://msdn.microsoft.com/63c6115e-24f8-4f35-8397-8be63110b21f">XTYP_POKE</a>



<a href="https://msdn.microsoft.com/e776b995-6a64-4398-9e29-c151f3ef4c1d">XTYP_REQUEST</a>
 

 

