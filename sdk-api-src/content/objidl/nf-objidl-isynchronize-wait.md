---
UID: NF:objidl.ISynchronize.Wait
title: ISynchronize::Wait
author: windows-sdk-content
description: Waits for the synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first.
old-location: com\isynchronize_wait.htm
tech.root: com
ms.assetid: 1abed0be-b4e3-41f4-af6c-e327ce934b59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISynchronize interface [COM],Wait method, ISynchronize.Wait, ISynchronize::Wait, Wait, Wait method [COM], Wait method [COM],ISynchronize interface, _com_isynchronize_wait, com.isynchronize_wait, objidlbase/ISynchronize::Wait
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISynchronize.Wait
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISynchronize::Wait


## -description


Waits for the synchronization object to be signaled or for a specified timeout period to elapse, whichever comes first.


## -parameters




### -param dwFlags [in]

The wait options. Possible values are taken from the <a href="https://msdn.microsoft.com/e6f8300c-f74b-4383-8ee5-519a0ed0b358">COWAIT_FLAGS</a> enumeration. 


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
<dt><b>RPC_E_CALLPENDING</b></dt>
</dl>
</td>
<td width="60%">
The time-out period elapsed before the synchronization object was signaled.

</td>
</tr>
</table>
 




## -remarks



If the caller is waiting in a single-thread apartment, <b>Wait</b> enters the COM modal loop. If the caller is waiting in a multithread apartment, the caller is blocked until <b>Wait</b> returns.




## -see-also




<a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>



<a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a>
 

 

