---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CreateTransactionManager function


## -description


Creates a new transaction manager (TM) object and returns a handle with the specified access.


## -parameters




### -param OPTIONAL

TBD




### -param LogFileName [in, optional]

The log file stream name.  If the stream does not exist in the log, it is created. To create a volatile TM, this parameter must be <b>NULL</b> and <i>CreateOptions</i> must specify TRANSACTION_MANAGER_VOLATILE, this transaction manager is considered volatile.


#### - CommitStrength [in, optional]

Reserved; specify zero.


#### - CreateOptions [in, optional]

Any optional attributes for the new TM.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRANSACTION_MANAGER_VOLATILE"></a><a id="transaction_manager_volatile"></a><dl>
<dt><b>TRANSACTION_MANAGER_VOLATILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the TM is volatile, and does not perform recovery.

</td>
</tr>
</table>
 


#### - lpTransactionAttributes [in, optional]

The transaction <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> (ACLs) for the TM object. 


## -returns



If the function succeeds, the return value is a handle to the transaction manager.  

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -remarks



Immediately after calling this function, you must call <a href="https://msdn.microsoft.com/6f217ebb-3423-41d3-acff-eb21838c9751">RecoverTransactionManager</a>.

If your transaction manager is volatile, all your your resource managers must also be volatile.

You must call <a href="https://msdn.microsoft.com/6f217ebb-3423-41d3-acff-eb21838c9751">RecoverTransactionManager</a> after creating a TM in order for the TM to function correctly.




## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/6b53609a-b956-441c-b5b5-9a8e6aa489c9">OpenTransactionManager</a>



<a href="https://msdn.microsoft.com/6f217ebb-3423-41d3-acff-eb21838c9751">RecoverTransactionManager</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

