---
UID: NF:d3d12.ID3D12Fence.SetEventOnCompletion
title: ID3D12Fence::SetEventOnCompletion
author: windows-sdk-content
description: Specifies an event that should be fired when the fence reaches a certain value.
old-location: direct3d12\id3d12fence_seteventoncompletion.htm
tech.root: direct3d12
ms.assetid: DBC5A1FD-F3D0-4C9B-965B-1967151093F7
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12Fence interface,SetEventOnCompletion method, ID3D12Fence.SetEventOnCompletion, ID3D12Fence::SetEventOnCompletion, SetEventOnCompletion, SetEventOnCompletion method, SetEventOnCompletion method,ID3D12Fence interface, d3d12/ID3D12Fence::SetEventOnCompletion, direct3d12.id3d12fence_seteventoncompletion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Fence.SetEventOnCompletion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12.h
: 
- ID3D12Fence.SetEventOnCompletion
: 
---

# ID3D12Fence::SetEventOnCompletion


## -description


Specifies an event that should be fired when the fence reaches a certain value.


## -parameters




### -param Value

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The fence value when the event is to be signaled.


### -param hEvent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a></b>

A handle to the event object.


## -returns



Type: <b>HRESULT</b>

This method returns <b>E_OUTOFMEMORY</b> if the kernel components don’t have sufficient memory to store the event in a list. See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.




## -remarks



To specify multiple fences before an event is triggered, refer to <a href="https://msdn.microsoft.com/C187EEB7-DCD0-4535-AF0E-EF2C0E2DC83C">SetEventOnMultipleFenceCompletion</a>.


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Multithreading</a> sample uses <b>ID3D12Fence::SetEventOnCompletion</b> as follows:
        


```cpp
// Wait for the command list to execute; we are reusing the same command 
// list in our main loop but for now, we just want to wait for setup to 
// complete before continuing.

// Signal and increment the fence value.
const UINT64 fenceToWaitFor = m_fenceValue;
ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fenceToWaitFor));
m_fenceValue++;

// Wait until the fence is completed.
ThrowIfFailed(m_fence->SetEventOnCompletion(fenceToWaitFor, m_fenceEvent));
WaitForSingleObject(m_fenceEvent, INFINITE);

```


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

