---
UID: NF:objidl.ISynchronizeContainer.WaitMultiple
title: ISynchronizeContainer::WaitMultiple
author: windows-sdk-content
description: Waits for any synchronization object in the container to be signaled or for a specified timeout period to elapse, whichever comes first.
old-location: com\isynchronizecontainer_waitmultiple.htm
tech.root: com
ms.assetid: 2754b744-3ba8-4e60-9847-1d0eb3c24180
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISynchronizeContainer interface [COM],WaitMultiple method, ISynchronizeContainer.WaitMultiple, ISynchronizeContainer::WaitMultiple, WaitMultiple, WaitMultiple method [COM], WaitMultiple method [COM],ISynchronizeContainer interface, _com_isynchronizecontainer_waitmultiple, com.isynchronizecontainer_waitmultiple, objidlbase/ISynchronizeContainer::WaitMultiple
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeContainer.WaitMultiple
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISynchronizeContainer::WaitMultiple


## -description


Waits for any synchronization object in the container to be signaled or for a specified timeout period to elapse, whichever comes first.


## -parameters




### -param dwFlags [in]

The wait options. Possible values are taken from the <a href="https://msdn.microsoft.com/e6f8300c-f74b-4383-8ee5-519a0ed0b358">COWAIT_FLAGS</a> enumeration. COWAIT_WAITALL is not a valid setting for this method.


### -param dwTimeOut [in]

The time this call will wait before returning, in milliseconds. If this parameter is INFINITE, the caller will wait until a synchronization object is signaled, no matter how long it takes. If this parameter is 0, the method returns immediately.


### -param ppSync [out]

A pointer to an <a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a> interface pointer on the synchronization object that was signaled. This parameter cannot be <b>NULL</b>.


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




<a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>



<a href="https://msdn.microsoft.com/6a5be504-b5fa-491c-ba65-74c5de39e263">ISynchronizeContainer</a>
 

 

