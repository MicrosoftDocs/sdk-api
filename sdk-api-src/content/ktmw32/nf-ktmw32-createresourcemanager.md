---
UID: NF:ktmw32.CreateResourceManager
title: CreateResourceManager function
author: windows-sdk-content
description: Creates a new resource manager (RM) object, and associates the RM with a transaction manager (TM).
old-location: fs\createresourcemanager.htm
old-project: ktm
ms.assetid: ad88e478-1dff-4f35-a0e3-6bda8bb45711
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateResourceManager, CreateResourceManager function [Files], RESOURCE_MANAGER_VOLATILE, fs.createresourcemanager, ktmw32/CreateResourceManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - CreateResourceManager
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# CreateResourceManager function


## -description


Creates a new resource manager (RM) object, and associates the RM with a transaction manager (TM).


## -parameters




### -param lpResourceManagerAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that contains the security attributes for the resource manager.  Specify <b>NULL</b> to obtain the default attributes.


### -param ResourceManagerId [in]

A pointer the resource manager GUID. This parameter is required and must not be <b>NULL</b>.


### -param CreateOptions [in, optional]

Any optional attributes for the new RM.  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RESOURCE_MANAGER_VOLATILE"></a><a id="resource_manager_volatile"></a><dl>
<dt><b>RESOURCE_MANAGER_VOLATILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the RM is volatile, and does not perform recovery.

</td>
</tr>
</table>
 


### -param TmHandle [in]

A handle to the TM that will manage the transactions for this RM.


### -param Description [in, optional]

A description for this RM.


## -returns



If the function succeeds, the return value is a handle to the RM.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the  possible error codes:






## -remarks



Immediately after calling this function, you must call <a href="https://msdn.microsoft.com/616ff873-c0d0-464e-9b1b-74a426b99abd">RecoverResourceManager</a>.

An RM is an endpoint for TM notifications regarding transactions that the RM has enlisted in.

RMs are typically persistent, meaning that after a system failure, they must be reopened  to perform certain operations. Volatile, or transient, RMs can be created by calling the <b>CreateResourceManager</b> function and by specifying RESOURCE_MANAGER_VOLATILE.  Volatile RMs do not perform recovery operations, but do require notifications about a transaction.

You can create a volatile RM on a durable TM, but you cannot create a durable RM on a volatile TM.




## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/396b586f-c594-4481-b095-862e9058519c">OpenResourceManager</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/219fc899-84ee-474f-9f86-6ebf9c721810">SetResourceManagerCompletionPort</a>
 

 

