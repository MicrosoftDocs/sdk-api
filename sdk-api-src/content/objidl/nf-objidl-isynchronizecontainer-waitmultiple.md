---
UID: NF:objidl.ISynchronizeContainer.WaitMultiple
title: ISynchronizeContainer::WaitMultiple (objidl.h)
description: The ISynchronizeContainer::WaitMultiple method (objidl.h) waits for a synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first.
helpviewer_keywords: ["ISynchronizeContainer interface [COM]","WaitMultiple method","ISynchronizeContainer.WaitMultiple","ISynchronizeContainer::WaitMultiple","WaitMultiple","WaitMultiple method [COM]","WaitMultiple method [COM]","ISynchronizeContainer interface","_com_isynchronizecontainer_waitmultiple","com.isynchronizecontainer_waitmultiple","objidlbase/ISynchronizeContainer::WaitMultiple"]
old-location: com\isynchronizecontainer_waitmultiple.htm
tech.root: com
ms.assetid: 2754b744-3ba8-4e60-9847-1d0eb3c24180
ms.date: 08/15/2022
ms.keywords: ISynchronizeContainer interface [COM],WaitMultiple method, ISynchronizeContainer.WaitMultiple, ISynchronizeContainer::WaitMultiple, WaitMultiple, WaitMultiple method [COM], WaitMultiple method [COM],ISynchronizeContainer interface, _com_isynchronizecontainer_waitmultiple, com.isynchronizecontainer_waitmultiple, objidlbase/ISynchronizeContainer::WaitMultiple
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISynchronizeContainer::WaitMultiple
 - objidl/ISynchronizeContainer::WaitMultiple
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeContainer.WaitMultiple
---

# ISynchronizeContainer::WaitMultiple


## -description

Waits for any synchronization object in the container to be signaled or for a specified timeout period to elapse, whichever comes first.

## -parameters

### -param dwFlags [in]

The wait options. Possible values are taken from the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_FLAGS</a> enumeration. COWAIT_WAITALL is not a valid setting for this method.

### -param dwTimeOut [in]

The time this call will wait before returning, in milliseconds. If this parameter is INFINITE, the caller will wait until a synchronization object is signaled, no matter how long it takes. If this parameter is 0, the method returns immediately.

### -param ppSync [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-isynchronize">ISynchronize</a> interface pointer on the synchronization object that was signaled. This parameter cannot be <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The synchronization object was signaled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out period elapsed before the synchronization object was signaled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_NO_SYNC</b></dt>
</dl>
</td>
<td width="60%">
There are no synchronization objects in the container.

</td>
</tr>
</table>

## -remarks

If the caller is waiting in a single-thread apartment, <b>WaitMultiple</b> enters the COM modal loop. If the caller is waiting in a multithread apartment, the caller is blocked until <b>WaitMultiple</b> returns.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizecontainer">ISynchronizeContainer</a>
