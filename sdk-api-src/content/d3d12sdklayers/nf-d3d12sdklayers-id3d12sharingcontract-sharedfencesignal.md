---
UID: NF:d3d12sdklayers.ID3D12SharingContract.SharedFenceSignal
title: ID3D12SharingContract::SharedFenceSignal
author: windows-sdk-content
description: Signals a shared fence between the D3D layers and diagnostics tools.
old-location: direct3d12\id3d12sharingcontract_sharedfencesignal.htm
old-project: direct3d12
ms.assetid: E90576A7-B665-4911-A17E-FD328CD71458
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ID3D12SharingContract interface,SharedFenceSignal method, ID3D12SharingContract.SharedFenceSignal, ID3D12SharingContract::SharedFenceSignal, SharedFenceSignal, SharedFenceSignal method, SharedFenceSignal method,ID3D12SharingContract interface, d3d12sdklayers/ID3D12SharingContract::SharedFenceSignal, direct3d12.id3d12sharingcontract_sharedfencesignal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
tech.root: 
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12SharingContract.SharedFenceSignal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12SharingContract::SharedFenceSignal


## -description


Signals a shared fence between the D3D layers and diagnostics tools.


## -parameters




### -param pFence [in]

Type: <b><a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>*</b>

A pointer to the shared fence to signal.


### -param FenceValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

An unsigned 64bit value to signal the shared fence with.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/10E61C88-0CDC-42E6-AB70-4911D254C40A">ID3D12SharingContract</a>
 

 

