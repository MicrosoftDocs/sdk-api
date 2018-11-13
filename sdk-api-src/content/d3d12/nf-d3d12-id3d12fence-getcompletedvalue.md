---
UID: NF:d3d12.ID3D12Fence.GetCompletedValue
title: ID3D12Fence::GetCompletedValue
author: windows-sdk-content
description: Gets the current value of the fence.
old-location: direct3d12\id3d12fence_getcompletedvalue.htm
tech.root: direct3d12
ms.assetid: 2F2DDFC5-8D31-4BCE-B378-610C95D7805F
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: GetCompletedValue, GetCompletedValue method, GetCompletedValue method,ID3D12Fence interface, ID3D12Fence interface,GetCompletedValue method, ID3D12Fence.GetCompletedValue, ID3D12Fence::GetCompletedValue, d3d12/ID3D12Fence::GetCompletedValue, direct3d12.id3d12fence_getcompletedvalue
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
 - ID3D12Fence.GetCompletedValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Fence::GetCompletedValue


## -description


Gets the current value of the fence.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Returns the current value of the fence. If the device has been removed, the return value will be <b>UINT64_MAX</b>.




## -see-also




<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

