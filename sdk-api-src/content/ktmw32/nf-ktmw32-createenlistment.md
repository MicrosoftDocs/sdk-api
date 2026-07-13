---
UID: NF:ktmw32.CreateEnlistment
title: CreateEnlistment function (ktmw32.h)
description: Creates an enlistment, sets its initial state, and opens a handle to the enlistment with the specified access.
helpviewer_keywords: ["CreateEnlistment","CreateEnlistment function [Files]","ENLISTMENT_SUPERIOR","fs.createenlistment","ktmw32/CreateEnlistment"]
old-location: fs\createenlistment.htm
tech.root: fs
ms.assetid: 7bc06468-947f-48ec-8e58-20df58ed93bd
ms.date: 12/05/2018
ms.keywords: CreateEnlistment, CreateEnlistment function [Files], ENLISTMENT_SUPERIOR, fs.createenlistment, ktmw32/CreateEnlistment
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
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateEnlistment
 - ktmw32/CreateEnlistment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - CreateEnlistment
---

# CreateEnlistment function


## -description

Creates an enlistment, sets its initial state, and opens a handle to the enlistment with the specified 
    access.

## -parameters

### -param lpEnlistmentAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
      structure that contains the security attributes for the enlistment manager.  Specify 
      <b>NULL</b> to obtain the default attributes.

### -param ResourceManagerHandle [in]

A handle to the resource manager (RM) to enlist.

### -param TransactionHandle [in]

A handle to the transaction in which the RM is enlisting.

### -param NotificationMask [in]

The notifications this RM is requesting for the <i>TransactionHandle</i> parameter. For 
      a list of valid values, see <a href="/windows/desktop/Ktm/notification-mask">NOTIFICATION_MASK</a>.

### -param CreateOptions [in, optional]

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

### -param EnlistmentKey [in, optional]

A pointer to a user-defined structure used by the RM that is returned when a notification is sent in the 
      <a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a> structure. This is 
      typically used to associate a private structure  with this specific transaction.

## -returns

If the function succeeds, the return value is a handle to the enlistment.
      

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

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
      pair of prepare and rollback notifications.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-commitcomplete">CommitComplete</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-commitenlistment">CommitEnlistment</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/Ktm/notification-mask">NOTIFICATION_MASK</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-openenlistment">OpenEnlistment</a>



<a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a>