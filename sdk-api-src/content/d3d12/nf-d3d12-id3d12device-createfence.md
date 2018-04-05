---
UID: NF:d3d12.ID3D12Device.CreateFence
title: ID3D12Device::CreateFence method
author: windows-driver-content
description: Creates a fence object.
old-location: direct3d12\id3d12device_createfence.htm
old-project: direct3d12
ms.assetid: 731A60CA-644A-4FC2-8461-DDD686363BED
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreateFence method, CreateFence method, ID3D12Device interface, CreateFence,ID3D12Device.CreateFence, ID3D12Device, ID3D12Device interface, CreateFence method, ID3D12Device::CreateFence, d3d12/ID3D12Device::CreateFence, direct3d12.id3d12device_createfence
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
-	D3D12.dll
api_name:
-	ID3D12Device.CreateFence
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Device::CreateFence method


## -description



          Creates a fence object.
        


## -parameters




### -param InitialValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>


            The initial value for the fence.
          


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/EF725566-B77A-40EE-B5E3-86C5D13CC7D5">D3D12_FENCE_FLAGS</a></b>


            A combination of <a href="https://msdn.microsoft.com/EF725566-B77A-40EE-B5E3-86C5D13CC7D5">D3D12_FENCE_FLAGS</a>-typed values that are combined by using a bitwise OR operation. 
            The resulting value specifies options for the fence.
          


### -param riid

Type: <b>REFIID</b>


            The globally unique identifier (<b>GUID</b>) for the fence interface (<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the fence can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12Fence) will get the <b>GUID</b> of the interface to a fence.
          


### -param ppFence [out]

Type: <b>void**</b>


            A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a> interface that is used to access the fence.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>


            Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

