---
UID: NF:objidl.ISynchronize.Wait
title: ISynchronize::Wait (objidl.h)
description: The ISynchronize::Wait method (objidl.h) waits for the synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first. 
helpviewer_keywords: ["ISynchronize interface [COM]","Wait method","ISynchronize.Wait","ISynchronize::Wait","Wait","Wait method [COM]","Wait method [COM]","ISynchronize interface","_com_isynchronize_wait","com.isynchronize_wait","objidlbase/ISynchronize::Wait"]
old-location: com\isynchronize_wait.htm
tech.root: com
ms.assetid: 1abed0be-b4e3-41f4-af6c-e327ce934b59
ms.date: 08/15/2022
ms.keywords: ISynchronize interface [COM],Wait method, ISynchronize.Wait, ISynchronize::Wait, Wait, Wait method [COM], Wait method [COM],ISynchronize interface, _com_isynchronize_wait, com.isynchronize_wait, objidlbase/ISynchronize::Wait
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
 - ISynchronize::Wait
 - objidl/ISynchronize::Wait
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
 - ISynchronize.Wait
---

# ISynchronize::Wait


## -description

Waits for the synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first.

## -parameters

### -param dwFlags [in]

The wait options. Possible values are taken from the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_FLAGS</a> enumeration.

### -param dwMilliseconds [in]

The time this call will wait before returning, in milliseconds. If this parameter is INFINITE, the caller will wait until the synchronization object is signaled, no matter how long it takes. If this parameter is 0, the method returns immediately.

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
<dt><b>RPC_S_CALLPENDING</b></dt>
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
There is no synchronization object to wait on.
</td>
</tr>
</table>

## -remarks

If the caller is waiting in a single-thread apartment, <b>Wait</b> enters the COM modal loop. If the caller is waiting in a multithread apartment, the caller is blocked until <b>Wait</b> returns.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isynchronize">ISynchronize</a>
