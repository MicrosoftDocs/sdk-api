---
UID: NF:d3d12.ID3D12Fence.GetCompletedValue
title: ID3D12Fence::GetCompletedValue (d3d12.h)
author: windows-sdk-content
description: Gets the current value of the fence.
old-location: direct3d12\id3d12fence_getcompletedvalue.htm
tech.root: direct3d12
ms.assetid: 2F2DDFC5-8D31-4BCE-B378-610C95D7805F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCompletedValue, GetCompletedValue method, GetCompletedValue method,ID3D12Fence interface, ID3D12Fence interface,GetCompletedValue method, ID3D12Fence.GetCompletedValue, ID3D12Fence::GetCompletedValue, d3d12/ID3D12Fence::GetCompletedValue, direct3d12.id3d12fence_getcompletedvalue
ms.topic: method
f1_keywords: ["d3d12/ID3D12Fence.GetCompletedValue"]
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
 - ID3D12Fence.GetCompletedValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Fence::GetCompletedValue


## -description


Gets the current value of the fence.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Returns the current value of the fence. If the device has been removed, the return value will be <b>UINT64_MAX</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/user-mode-heap-synchronization">Synchronization and Multi-Engine</a>
 

 

