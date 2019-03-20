---
UID: NF:d3d11_4.ID3D11Device5.CreateFence
title: ID3D11Device5::CreateFence (d3d11_4.h)
author: windows-sdk-content
description: Creates a fence object.
old-location: direct3d11\id3d11device5_createfence.htm
tech.root: direct3d11
ms.assetid: B4AA9E0D-AAF4-4632-A98F-A3212764D5E1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFence, CreateFence method [Direct3D 11], CreateFence method [Direct3D 11],ID3D11Device5 interface, ID3D11Device5 interface [Direct3D 11],CreateFence method, ID3D11Device5.CreateFence, ID3D11Device5::CreateFence, d3d11_4/ID3D11Device5::CreateFence, direct3d11.id3d11device5_createfence
ms.topic: method
req.header: d3d11_4.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device5.CreateFence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device5::CreateFence


## -description


Creates a fence object.

This member function is equivalent to the Direct3D 12 <a href="https://msdn.microsoft.com/731A60CA-644A-4FC2-8461-DDD686363BED">ID3D12Device::CreateFence</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.


## -parameters




### -param InitialValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The initial value for the fence.
          


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/745B72A2-628C-477E-8534-336E73B5268A">D3D11_FENCE_FLAG</a></b>

A combination of <a href="https://msdn.microsoft.com/745B72A2-628C-477E-8534-336E73B5268A">D3D11_FENCE_FLAG</a>-typed values that are combined by using a bitwise OR operation. 
            The resulting value specifies options for the fence.
          


### -param ReturnedInterface

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the fence interface (<a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the fence can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D11Fence) will get the <b>GUID</b> of the interface to a fence.
          


### -param ppFence [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a> interface that is used to access the fence.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/C077BAD4-08D2-4F1F-8313-5066F68F014C">ID3D11Device5</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt589892(v=VS.85).aspx">UnregisterDeviceRemoved</a>
 

 

