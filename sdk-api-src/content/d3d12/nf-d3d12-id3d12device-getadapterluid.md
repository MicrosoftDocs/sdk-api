---
UID: NF:d3d12.ID3D12Device.GetAdapterLuid
title: ID3D12Device::GetAdapterLuid method
author: windows-driver-content
description: Gets a locally unique identifier for the current device (adapter).
old-location: direct3d12\id3d12device_getadapterluid.htm
old-project: direct3d12
ms.assetid: 006E72E0-AE09-4834-9ACB-D48698050BF2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetAdapterLuid method, GetAdapterLuid method, ID3D12Device interface, GetAdapterLuid,ID3D12Device.GetAdapterLuid, ID3D12Device, ID3D12Device interface, GetAdapterLuid method, ID3D12Device::GetAdapterLuid, d3d12/ID3D12Device::GetAdapterLuid, direct3d12.id3d12device_getadapterluid
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12Device.GetAdapterLuid
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12Device::GetAdapterLuid method


## -description



          Gets a locally unique identifier for the current device (adapter).
        


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a></b>


            The locally unique identifier for the adapter.
          




## -remarks




          This method returns a unique identifier for the adapter that is specific to the adapter hardware.
          Applications can use this identifier to define robust mappings across various APIs (Direct3D 12, DXGI).
        


          A locally unique identifier (LUID) is a 64-bit value that is guaranteed to be unique only on the system on which it was generated.
          The uniqueness of a locally unique identifier (LUID) is guaranteed only until the system is restarted.
        




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

