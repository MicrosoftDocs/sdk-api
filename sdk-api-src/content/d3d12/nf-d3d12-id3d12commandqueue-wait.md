---
UID: NF:d3d12.ID3D12CommandQueue.Wait
title: ID3D12CommandQueue::Wait
author: windows-sdk-content
description: Waits until the specified fence reaches or exceeds the specified value.
old-location: direct3d12\id3d12commandqueue_wait.htm
tech.root: direct3d12
ms.assetid: 75D494D0-BCEC-453E-AB4F-E57CE2C9B318
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12CommandQueue interface,Wait method, ID3D12CommandQueue.Wait, ID3D12CommandQueue::Wait, Wait, Wait method, Wait method,ID3D12CommandQueue interface, d3d12/ID3D12CommandQueue::Wait, direct3d12.id3d12commandqueue_wait
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
 - ID3D12CommandQueue.Wait
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12CommandQueue::Wait


## -description


Waits until the specified fence reaches or exceeds the specified value.


## -parameters




### -param pFence

Type: <b><a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a> object.
          


### -param Value

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The value that the command queue is waiting for the fence to reach or exceed.  So when  <a href="https://msdn.microsoft.com/2F2DDFC5-8D31-4BCE-B378-610C95D7805F">ID3D12Fence::GetCompletedValue</a> is greater than or equal to <i>Value</i>, the wait is terminated.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

