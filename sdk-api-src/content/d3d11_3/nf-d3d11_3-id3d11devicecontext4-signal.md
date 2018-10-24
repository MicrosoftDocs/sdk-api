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
---

# ID3D11DeviceContext4::Signal


## -description


Updates a fence to a specified value after all previous work has completed.

This member function is equivalent to the Direct3D 12 <a href="https://msdn.microsoft.com/en-us/library/Dn899171(v=VS.85).aspx">ID3D12CommandQueue::Signal</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.
<div class="alert"><b>Note</b>  This method only applies to immediate-mode contexts.</div><div> </div>

## -parameters




### -param pFence

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Mt492484(v=VS.85).aspx">ID3D11Fence</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Mt492484(v=VS.85).aspx">ID3D11Fence</a> object.
          


### -param Value

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT64</a></b>

The value to set the fence to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt492481(v=VS.85).aspx">ID3D11DeviceContext4</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899217(v=VS.85).aspx">Synchronization and Multi-Engine (Direct3D 12)</a>
 

 

