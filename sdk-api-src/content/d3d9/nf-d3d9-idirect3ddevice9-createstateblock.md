---
UID: NF:d3d9.IDirect3DDevice9.CreateStateBlock
title: IDirect3DDevice9::CreateStateBlock
author: windows-sdk-content
description: Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states.
old-location: direct3d9\idirect3ddevice9__createstateblock.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createstateblock.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: CreateStateBlock, CreateStateBlock method [Direct3D 9], CreateStateBlock method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateStateBlock method, IDirect3DDevice9.CreateStateBlock, IDirect3DDevice9::CreateStateBlock, bc860c8f-4665-5146-40bc-db147a89e0b4, d3d9helper/IDirect3DDevice9::CreateStateBlock, direct3d9.idirect3ddevice9__createstateblock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.CreateStateBlock
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::CreateStateBlock


## -description


Creates a new state block that contains the values for all device states, vertex-related states, or pixel-related states.


## -parameters




### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172608(v=VS.85).aspx">D3DSTATEBLOCKTYPE</a></b>

Type of state data that the method should capture. This parameter can be set to a value defined in the <a href="https://msdn.microsoft.com/library/Bb172608(v=VS.85).aspx">D3DSTATEBLOCKTYPE</a> enumerated type. 


### -param ppSB [out, retval]

Type: <b><a href="https://msdn.microsoft.com/library/Bb205887(v=VS.85).aspx">IDirect3DStateBlock9</a>**</b>

Pointer to a state block interface. See <a href="https://msdn.microsoft.com/library/Bb205887(v=VS.85).aspx">IDirect3DStateBlock9</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



Vertex-related device states typically refer to those states that affect how the system processes vertices. Pixel-related states generally refer to device states that affect how the system processes pixel or depth-buffer data during rasterization. Some states are contained in both groups. 

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

In Direct3D 9, a state block contains state data, for the states it was requested to capture, when the object is created. To change the value of the state block, call <a href="https://msdn.microsoft.com/library/Bb205890(v=VS.85).aspx">IDirect3DStateBlock9::Capture</a> or <a href="https://msdn.microsoft.com/library/Bb174351(v=VS.85).aspx">IDirect3DDevice9::BeginStateBlock</a>/<a href="https://msdn.microsoft.com/library/Bb174376(v=VS.85).aspx">IDirect3DDevice9::EndStateBlock</a>. There is no state saved when a state block object is created in Direct3D 10.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/library/Bb174351(v=VS.85).aspx">IDirect3DDevice9::BeginStateBlock</a>



<a href="https://msdn.microsoft.com/library/Bb174376(v=VS.85).aspx">IDirect3DDevice9::EndStateBlock</a>
 

 

