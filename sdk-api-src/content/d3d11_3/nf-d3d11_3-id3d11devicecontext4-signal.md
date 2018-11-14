---
UID: NF:d3d11_3.ID3D11DeviceContext4.Signal
title: ID3D11DeviceContext4::Signal
author: windows-sdk-content
description: Updates a fence to a specified value after all previous work has completed.
old-location: direct3d11\id3d11devicecontext4_signal.htm
tech.root: direct3d11
ms.assetid: 5B308187-27B1-40B8-B9B7-CD8A8223A0EE
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11DeviceContext4 interface [Direct3D 11],Signal method, ID3D11DeviceContext4.Signal, ID3D11DeviceContext4::Signal, Signal, Signal method [Direct3D 11], Signal method [Direct3D 11],ID3D11DeviceContext4 interface, d3d11_3/ID3D11DeviceContext4::Signal, direct3d11.id3d11devicecontext4_signal
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext4.Signal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11_3.h
: 
- ID3D11DeviceContext4.Signal
: 
---

# ID3D11DeviceContext4::Signal


## -description


Updates a fence to a specified value after all previous work has completed.

This member function is equivalent to the Direct3D 12 <a href="https://msdn.microsoft.com/487E2DED-C741-4376-9EE2-3DDD2F4F76BB">ID3D12CommandQueue::Signal</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.
<div class="alert"><b>Note</b>  This method only applies to immediate-mode contexts.</div><div> </div>

## -parameters




### -param pFence

Type: <b><a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a> object.
          


### -param Value

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

The value to set the fence to.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/9A4B737C-C0A8-4319-A9CA-8172E992774D">ID3D11DeviceContext4</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine (Direct3D 12)</a>
 

 

