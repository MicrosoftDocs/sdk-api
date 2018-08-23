---
UID: NF:d3d9helper.IDirect3DVertexBuffer9.Lock
title: IDirect3DVertexBuffer9::Lock
author: windows-sdk-content
description: Locks a range of vertex data and obtains a pointer to the vertex buffer memory.
old-location: direct3d9\idirect3dvertexbuffer9__lock.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexbuffer9__lock.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 50b9d9ea-bb70-b92b-dbd4-0e355b29ab40, IDirect3DVertexBuffer9 interface [Direct3D 9],Lock method, IDirect3DVertexBuffer9.Lock, IDirect3DVertexBuffer9::Lock, Lock, Lock method [Direct3D 9], Lock method [Direct3D 9],IDirect3DVertexBuffer9 interface, d3d9helper/IDirect3DVertexBuffer9::Lock, direct3d9.idirect3dvertexbuffer9__lock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DVertexBuffer9.Lock
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVertexBuffer9::Lock


## -description


Locks a range of vertex data and obtains a pointer to the vertex buffer memory.


## -parameters




### -param OffsetToLock [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Offset into the vertex data to lock, in bytes. To lock the entire vertex buffer, specify 0 for both parameters, SizeToLock and OffsetToLock.


### -param SizeToLock [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the vertex data to lock, in bytes. To lock the entire vertex buffer, specify 0 for both parameters, SizeToLock and OffsetToLock.


### -param ppbData [out]

Type: <b>VOID**</b>

VOID* pointer to a memory buffer containing the returned vertex data. 


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 
    


<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
<li>D3DLOCK_NOOVERWRITE</li>
</ul>
For a description of the flags, see <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



As a general rule, do not hold a lock across more than one frame. When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls. DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.

The D3DLOCK_DISCARD and D3DLOCK_NOOVERWRITE flags are valid only on buffers created with D3DUSAGE_DYNAMIC.

For information about using D3DLOCK_DISCARD or D3DLOCK_NOOVERWRITE with <b>IDirect3DVertexBuffer9::Lock</b>, see <a href="https://msdn.microsoft.com/074f848e-4a42-48a2-adf7-4026b8967413">Using Dynamic Vertex and Index Buffers</a>.




## -see-also




<a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>



<a href="https://msdn.microsoft.com/72932c97-d515-4f50-94ec-274274248cd4">IDirect3DVertexBuffer9::Unlock</a>



<a href="https://msdn.microsoft.com/f9274562-413c-4f0d-bdb4-dc8fa83b6063">Vertex Buffers (Direct3D 9)</a>
 

 

