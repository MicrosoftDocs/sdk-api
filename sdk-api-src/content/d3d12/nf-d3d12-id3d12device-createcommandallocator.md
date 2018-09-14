---
UID: NF:d3d12.ID3D12Device.CreateCommandAllocator
title: ID3D12Device::CreateCommandAllocator
author: windows-sdk-content
description: Creates a command allocator object.
old-location: direct3d12\id3d12device_createcommandallocator.htm
tech.root: direct3d12
ms.assetid: 28DA0D59-3DB7-4652-B1EA-3360EA85A659
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateCommandAllocator, CreateCommandAllocator method, CreateCommandAllocator method,ID3D12Device interface, ID3D12Device interface,CreateCommandAllocator method, ID3D12Device.CreateCommandAllocator, ID3D12Device::CreateCommandAllocator, d3d12/ID3D12Device::CreateCommandAllocator, direct3d12.id3d12device_createcommandallocator
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
 - ID3D12Device.CreateCommandAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateCommandAllocator


## -description


Creates a command allocator object.


## -parameters




### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE</a></b>

A <a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE</a>-typed value that specifies the type of command allocator to create.
            The type of command allocator can be the type that records either direct command lists or bundles.
          


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the command allocator interface (<a href="https://msdn.microsoft.com/ADC494E6-1698-415D-90C5-F99FCD4C5309">ID3D12CommandAllocator</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the command allocator can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12CommandAllocator) will get the <b>GUID</b> of the interface to a command allocator.
          


### -param ppCommandAllocator [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/ADC494E6-1698-415D-90C5-F99FCD4C5309">ID3D12CommandAllocator</a> interface for the command allocator.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the command allocator.
              See <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> for other possible return values.
            




## -remarks



The device creates command lists from the command allocator.
      


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommandAllocator</b> as follows:
        


```cpp
ThrowIfFailed(pDevice->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
ThrowIfFailed(pDevice->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_BUNDLE, IID_PPV_ARGS(&m_bundleAllocator)));

```


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

