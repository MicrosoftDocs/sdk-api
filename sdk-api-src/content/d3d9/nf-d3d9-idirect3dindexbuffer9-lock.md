---
UID: NF:d3d9.IDirect3DIndexBuffer9.Lock
title: IDirect3DIndexBuffer9::Lock (d3d9.h)
author: windows-sdk-content
description: Locks a range of index data and obtains a pointer to the index buffer memory.
old-location: direct3d9\idirect3dindexbuffer9__lock.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dindexbuffer9__lock.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirect3DIndexBuffer9 interface [Direct3D 9],Lock method, IDirect3DIndexBuffer9.Lock, IDirect3DIndexBuffer9::Lock, Lock, Lock method [Direct3D 9], Lock method [Direct3D 9],IDirect3DIndexBuffer9 interface, a727fd78-b27c-1dcd-d6ca-d3bf644edaa8, d3d9helper/IDirect3DIndexBuffer9::Lock, direct3d9.idirect3dindexbuffer9__lock
ms.topic: method
f1_keywords: 
 - "d3d9/IDirect3DIndexBuffer9.Lock"
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DIndexBuffer9.Lock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DIndexBuffer9::Lock


## -description


Locks a range of index data and obtains a pointer to the index buffer memory.


## -parameters




### -param OffsetToLock [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset into the index data to lock, in bytes. Lock the entire index buffer by specifying 0 for both parameters, SizeToLock and OffsetToLock. 


### -param SizeToLock [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of the index data to lock, in bytes. Lock the entire index buffer by specifying 0 for both parameters, SizeToLock and OffsetToLock.


### -param ppbData [out]

Type: <b>VOID**</b>

VOID* pointer to a memory buffer containing the returned index data. 


### -param Flags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Combination of zero or more locking flags that describe the type of lock to perform. For this method, the valid flags are: 
    


<ul>
<li>D3DLOCK_DISCARD</li>
<li>D3DLOCK_NO_DIRTY_UPDATE</li>
<li>D3DLOCK_NOSYSLOCK</li>
<li>D3DLOCK_READONLY</li>
<li>D3DLOCK_NOOVERWRITE</li>
</ul>
For a description of the flags, see <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dlock">D3DLOCK</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



As a general rule, do not hold a lock across more than one frame. When working with index buffers, you are allowed to make multiple lock calls. However, you must ensure that the number of lock calls match the number of unlock calls. <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawindexedprimitive">IDirect3DDevice9::DrawIndexedPrimitive</a> calls will not succeed with any outstanding lock count on any currently set index buffer. 

The D3DLOCK_DISCARD and D3DLOCK_NOOVERWRITE flags are valid only on buffers created with D3DUSAGE_DYNAMIC.

See <a href="https://docs.microsoft.com/windows/desktop/direct3d9/programming-tips">Programming Tips (Direct3D 9)</a> for information about using D3DLOCK_DISCARD or D3DLOCK_NOOVERWRITE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9">IDirect3DIndexBuffer9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock">IDirect3DIndexBuffer9::Unlock</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
 

 

