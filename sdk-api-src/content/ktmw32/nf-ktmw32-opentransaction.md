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

# OpenTransaction function


## -description


Opens an existing transaction.


## -parameters




### -param dwDesiredAccess [in]

The access to the transaction object. You must have read and write access to work with a transaction. See <a href="https://msdn.microsoft.com/93ef3098-b3cc-4b24-ae82-1c10d937f14f">Transaction Access Masks</a> for a list of valid values.   


### -param TransactionId [in]

The GUID that identifies the transaction to be opened. This is commonly referred to as  a unit of work for the transaction.


## -returns



If the function succeeds, the return value is a handle to the transaction.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the  possible error codes: 




## -remarks




        Clients close the transaction handle by using the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function. If the last transaction handle is closed without anyone calling the <a href="https://msdn.microsoft.com/17db5e1f-685b-46f0-bac6-dff4c18bb515">CommitTransaction</a> function on the transaction, then the KTM implicitly rolls back the transaction.




## -see-also




<a href="https://msdn.microsoft.com/17db5e1f-685b-46f0-bac6-dff4c18bb515">CommitTransaction</a>



<a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/7d3522b8-ddf0-449e-8ab4-09e679ba1f15">RollbackTransaction</a>



<a href="https://msdn.microsoft.com/93ef3098-b3cc-4b24-ae82-1c10d937f14f">Transaction Access Masks</a>
 

 

