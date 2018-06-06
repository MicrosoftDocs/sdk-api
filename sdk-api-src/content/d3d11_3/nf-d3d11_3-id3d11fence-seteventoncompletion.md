---
UID: NF:d3d11_3.ID3D11Fence.SetEventOnCompletion
title: ID3D11Fence::SetEventOnCompletion
author: windows-sdk-content
description: Specifies an event that should be fired when the fence reaches a certain value.
old-location: direct3d11\id3d11fence_seteventoncompletion.htm
old-project: direct3d11
ms.assetid: 255FF723-85FA-4230-B751-B5F52A6F8EBB
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: ID3D11Fence interface [Direct3D 11],SetEventOnCompletion method, ID3D11Fence.SetEventOnCompletion, ID3D11Fence::SetEventOnCompletion, SetEventOnCompletion, SetEventOnCompletion method [Direct3D 11], SetEventOnCompletion method [Direct3D 11],ID3D11Fence interface, d3d11_3/ID3D11Fence::SetEventOnCompletion, direct3d11.id3d11fence_seteventoncompletion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_3.h
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
tech.root: 
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11Fence.SetEventOnCompletion
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# ID3D11Fence::SetEventOnCompletion


## -description


Specifies an event that should be fired when the fence reaches a certain value.

This member function is equivalent to the Direct3D 12 <a href="https://msdn.microsoft.com/DBC5A1FD-F3D0-4C9B-965B-1967151093F7">ID3D12Fence::SetEventOnCompletion</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.


## -parameters




### -param Value

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The fence value when the event is to be signaled.


### -param hEvent

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a></b>

A handle to the event object.


## -returns



Type: <b>HRESULT</b>

This method returns <b>E_OUTOFMEMORY</b> if the kernel components don’t have sufficient memory to store the event in a list. See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.




## -see-also




<a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine (Direct3D 12)</a>
 

 

