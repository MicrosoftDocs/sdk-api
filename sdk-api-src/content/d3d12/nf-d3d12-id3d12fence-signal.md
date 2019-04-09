---
UID: NF:d3d12.ID3D12Fence.Signal
title: ID3D12Fence::Signal (d3d12.h)
author: windows-sdk-content
description: Sets the fence to the specified value.
old-location: direct3d12\id3d12fence_signal.htm
tech.root: direct3d12
ms.assetid: 8AC955C1-37C9-47F3-B35C-980783C58390
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12Fence interface,Signal method, ID3D12Fence.Signal, ID3D12Fence::Signal, Signal, Signal method, Signal method,ID3D12Fence interface, d3d12/ID3D12Fence::Signal, direct3d12.id3d12fence_signal
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
 - ID3D12Fence.Signal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Fence::Signal


## -description


Sets the fence to the specified value.


## -parameters




### -param Value

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The value to set the fence to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 




## -remarks



Use this method to set a fence value from the CPU side. Use <a href="https://msdn.microsoft.com/487E2DED-C741-4376-9EE2-3DDD2F4F76BB">ID3D12CommandQueue::Signal</a> to set a fence from the GPU side.




## -see-also




<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

