---
UID: NF:ktmw32.CreateResourceManager
title: CreateResourceManager function (ktmw32.h)
description: Creates a new resource manager (RM) object, and associates the RM with a transaction manager (TM).
helpviewer_keywords: ["CreateResourceManager","CreateResourceManager function [Files]","RESOURCE_MANAGER_VOLATILE","fs.createresourcemanager","ktmw32/CreateResourceManager"]
old-location: fs\createresourcemanager.htm
tech.root: fs
ms.assetid: ad88e478-1dff-4f35-a0e3-6bda8bb45711
ms.date: 12/05/2018
ms.keywords: CreateResourceManager, CreateResourceManager function [Files], RESOURCE_MANAGER_VOLATILE, fs.createresourcemanager, ktmw32/CreateResourceManager
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
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateResourceManager
 - ktmw32/CreateResourceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - CreateResourceManager
---

# CreateResourceManager function


## -description

Creates a new resource manager (RM) object, and associates the RM with a transaction manager (TM).

## -parameters

### -param lpResourceManagerAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that contains the security attributes for the resource manager.  Specify <b>NULL</b> to obtain the default attributes.

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

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the  possible error codes:

## -remarks

Immediately after calling this function, you must call <a href="/windows/desktop/api/ktmw32/nf-ktmw32-recoverresourcemanager">RecoverResourceManager</a>.

An RM is an endpoint for TM notifications regarding transactions that the RM has enlisted in.

RMs are typically persistent, meaning that after a system failure, they must be reopened  to perform certain operations. Volatile, or transient, RMs can be created by calling the <b>CreateResourceManager</b> function and by specifying RESOURCE_MANAGER_VOLATILE.  Volatile RMs do not perform recovery operations, but do require notifications about a transaction.

You can create a volatile RM on a durable TM, but you cannot create a durable RM on a volatile TM.

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-openresourcemanager">OpenResourceManager</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-setresourcemanagercompletionport">SetResourceManagerCompletionPort</a>