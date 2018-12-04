---
UID: NC:ddeml.PFNCALLBACK
title: PFNCALLBACK
author: windows-sdk-content
description: An application-defined callback function used with the Dynamic Data Exchange Management Library (DDEML) functions.
old-location: dataxchg\ddecallback.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecallback.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PFNCALLBACK, PFNCALLBACK callback, PFNCALLBACK callback function [Data Exchange], XCLASS_BOOL, XCLASS_DATA, XCLASS_FLAGS, XCLASS_NOTIFICATION, _win32_DdeCallback, _win32_ddecallback_cpp, dataxchg.ddecallback, ddeml/PFNCALLBACK, winui._win32_ddecallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFNCALLBACK callback function


## -description


An application-defined callback function used with the <a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a> (DDEML) functions. It processes Dynamic Data Exchange (DDE) transactions. The 
			<b>PFNCALLBACK</b> type defines a pointer to this callback function. <i>DdeCallback</i> is a placeholder for the application-defined function name. 


## -parameters




### -param wType


### -param wFmt


### -param hConv


### -param hsz1 [in]

Type: <b>HSZ</b>

A handle to a string. The meaning of this parameter depends on the type of the current transaction. For the meaning of this parameter, see the description of the transaction type. 


### -param hsz2 [in]

Type: <b>HSZ</b>

A handle to a string. The meaning of this parameter depends on the type of the current transaction. For the meaning of this parameter, see the description of the transaction type. 


### -param hData


### -param dwData1 [in]

Type: <b>ULONG_PTR</b>

Transaction-specific data. For the meaning of this parameter, see the description of the transaction type. 


### -param dwData2 [in]

Type: <b>ULONG_PTR</b>

Transaction-specific data. For the meaning of this parameter, see the description of the transaction type. 


#### - hconv [in]

Type: <b>HCONV</b>

A handle to the conversation associated with the current transaction. 


#### - hdata [in]

Type: <b>HDDEDATA</b>

A handle to DDE data. The meaning of this parameter depends on the type of the current transaction. For the meaning of this parameter, see the description of the transaction type. 


#### - uFmt [in]

Type: <b>UINT</b>

The format in which data is sent or received. 


#### - uType [in]

Type: <b>UINT</b>

The type of the current transaction. This parameter consists of a combination of transaction class flags and transaction type flags. The following table describes each of the transaction classes and provides a list of the transaction types in each class. For information about a specific transaction type, see the individual description of that type. 



#### XCLASS_BOOL

A DDE callback function should return <b>TRUE</b> or <b>FALSE</b> when it finishes processing a transaction that belongs to this class. The <b>XCLASS_BOOL</b> transaction class consists of the following types: 
                        

<ul>
<li>
<a href="https://msdn.microsoft.com/8911e722-5656-4ca6-8b0a-6bdf8281611a">XTYP_ADVSTART</a>
</li>
<li>
<a href="https://msdn.microsoft.com/74f43b10-f7ac-4370-9caa-7b9ddf3413ed">XTYP_CONNECT</a>
</li>
</ul>


#### XCLASS_DATA

A DDE callback function should return a DDE handle, the <b>CBR_BLOCK</b> return code, or <b>NULL</b> when it finishes processing a transaction that belongs to this class. The <b>XCLASS_DATA</b> transaction class consists of the following types: 
                        

<ul>
<li>
<a href="https://msdn.microsoft.com/9bd43e61-cbd6-4d53-bab3-90e85819b16b">XTYP_ADVREQ</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e776b995-6a64-4398-9e29-c151f3ef4c1d">XTYP_REQUEST</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4651e14f-ca13-412e-853d-326a13db78e4">XTYP_WILDCONNECT</a>
</li>
</ul>


#### XCLASS_FLAGS

A DDE callback function should return <b>DDE_FACK</b>, <b>DDE_FBUSY</b>, or <b>DDE_FNOTPROCESSED</b> when it finishes processing a transaction that belongs to this class. The <b>XCLASS_FLAGS</b> transaction class consists of the following types:
                        

<ul>
<li>
<a href="https://msdn.microsoft.com/c6e61785-b98c-4ffa-9d23-339e1c66cb4d">XTYP_ADVDATA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6001eb7d-59c0-49ec-97ce-26132891188c">XTYP_EXECUTE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/63c6115e-24f8-4f35-8397-8be63110b21f">XTYP_POKE</a>
</li>
</ul>


#### XCLASS_NOTIFICATION

The transaction types that belong to this class are for notification purposes only. The return value from the callback function is ignored. The <b>XCLASS_NOTIFICATION</b> transaction class consists of the following types: 
						

<ul>
<li>
<a href="https://msdn.microsoft.com/67dfa463-6a44-43a5-93be-a39c19c87c1c">XTYP_ADVSTOP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4db67539-9322-44d7-bf2b-749bd6cfcbb4">XTYP_CONNECT_CONFIRM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/22a9ec63-8a74-4829-ad02-d07dd0e8fa9b">XTYP_DISCONNECT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/710daa04-ed83-42e3-a55e-6ccf891a3d52">XTYP_ERROR</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a27791b1-c1b4-4516-b050-71da164fa80a">XTYP_MONITOR</a>
</li>
<li>
<a href="https://msdn.microsoft.com/465e9c10-1526-4e2a-8a46-5984043f5a93">XTYP_REGISTER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d34a6fab-0e3c-44fe-b25f-7011228fe261">XTYP_XACT_COMPLETE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a57a5d53-7919-4698-8c84-6142dd29bb2a">XTYP_UNREGISTER</a>
</li>
</ul>

## -returns



Type: <b>HDDEDATA</b>

The return value depends on the transaction class. For more information about the return values, see descriptions of the individual transaction types. 




## -remarks



The callback function is called asynchronously for transactions that do not involve the creation or termination of conversations. An application that does not frequently accept incoming messages will have reduced DDE performance because the Dynamic Data Exchange Management Library (DDEML) uses messages to initiate transactions. 

An application must register the callback function by specifying a pointer to the function in a call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1fb9c17b-829a-4c7e-947b-41b15b0db142">DdeEnableCallback</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

