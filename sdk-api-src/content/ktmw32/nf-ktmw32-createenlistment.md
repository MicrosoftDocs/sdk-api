---
UID: NF:ktmw32.CreateEnlistment
title: CreateEnlistment function
author: windows-sdk-content
description: Creates an enlistment, sets its initial state, and opens a handle to the enlistment with the specified access.
old-location: fs\createenlistment.htm
old-project: Ktm
ms.assetid: 7bc06468-947f-48ec-8e58-20df58ed93bd
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CreateEnlistment, CreateEnlistment function [Files], ENLISTMENT_SUPERIOR, fs.createenlistment, ktmw32/CreateEnlistment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ktmw32.h
req.include-header: 
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
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	KtmW32.dll
api_name:
-	CreateEnlistment
product: Windows
targetos: Windows
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
req.product: GDI+ 1.1
---

# CreateEnlistment function


## -description


Creates an enlistment, sets its initial state, and opens a handle to the enlistment with the specified 
    access.


## -parameters




### -param OPTIONAL

TBD




### -param ResourceManagerHandle [in]

A handle to the resource manager (RM) to enlist.


### -param TransactionHandle [in]

A handle to the transaction in which the RM is enlisting.


### -param NotificationMask [in]

The notifications this RM is requesting for the <i>TransactionHandle</i> parameter. For 
      a list of valid values, see <a href="https://msdn.microsoft.com/65db8ba5-193c-439b-8e8c-6cb4a9bd4efd">NOTIFICATION_MASK</a>.


#### - CreateOptions [in, optional]

Any optional enlistment instructions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ENLISTMENT_SUPERIOR"></a><a id="enlistment_superior"></a><dl>
<dt><b>ENLISTMENT_SUPERIOR</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Enlist as a superior transaction manager.

</td>
</tr>
</table>
 


#### - EnlistmentKey [in, optional]

A pointer to a user-defined structure used by the RM that is returned when a notification is sent in the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff564813">TRANSACTION_NOTIFICATION</a> structure. This is 
      typically used to associate a private structure  with this specific transaction.


#### - lpEnlistmentrAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
      structure that contains the security attributes for the enlistment manager.  Specify 
      <b>NULL</b> to obtain the default attributes.


## -returns



If the function succeeds, the return value is a handle to the enlistment.
      

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the  possible error codes:




## -remarks



<b>Windows Vista:  </b>Any attempt to enlist during the pre-prepare phase or later will fail.

If you do not specify within your notification mask that you accept a single-phase commit request, KTM always 
    performs a two-phase commit operation.

Keep the following notification rules in mind when enlisting in transactions:

<ul>
<li>The RM must always request rollback notification.</li>
<li>If the RM requests prepare notification, it must also request commit notification.</li>
<li>If the RM requests a single-phase commit operation, it must also specify prepare and commit 
      notifications.</li>
<li>The only time an RM is not required to request commit notifications is when it is requesting at least a 
      pair of preprepare and rollback notifications.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/de3e3a26-3e56-4732-8e7c-945b45593aed">CommitComplete</a>



<a href="https://msdn.microsoft.com/d1e1043d-2db3-4f05-affc-2d32744baf10">CommitEnlistment</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/65db8ba5-193c-439b-8e8c-6cb4a9bd4efd">NOTIFICATION_MASK</a>



<a href="https://msdn.microsoft.com/2c403e22-3feb-415a-b65b-572802764548">OpenEnlistment</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564813">TRANSACTION_NOTIFICATION</a>
 

 

