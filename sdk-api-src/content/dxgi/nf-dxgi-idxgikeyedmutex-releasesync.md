---
UID: NF:dxgi.IDXGIKeyedMutex.ReleaseSync
title: IDXGIKeyedMutex::ReleaseSync (dxgi.h)
description: Using a key, releases exclusive rendering access to a shared resource.
helpviewer_keywords: ["33872a53-bb15-32f2-c1f4-cfc8bdbac157","IDXGIKeyedMutex interface [DXGI]","ReleaseSync method","IDXGIKeyedMutex.ReleaseSync","IDXGIKeyedMutex::ReleaseSync","ReleaseSync","ReleaseSync method [DXGI]","ReleaseSync method [DXGI]","IDXGIKeyedMutex interface","direct3ddxgi.idxgikeyedmutex_releasesync","dxgi/IDXGIKeyedMutex::ReleaseSync"]
old-location: direct3ddxgi\idxgikeyedmutex_releasesync.htm
tech.root: direct3ddxgi
ms.assetid: 324741c9-33f2-4420-8c3f-4984e2ca0962
ms.date: 12/05/2018
ms.keywords: 33872a53-bb15-32f2-c1f4-cfc8bdbac157, IDXGIKeyedMutex interface [DXGI],ReleaseSync method, IDXGIKeyedMutex.ReleaseSync, IDXGIKeyedMutex::ReleaseSync, ReleaseSync, ReleaseSync method [DXGI], ReleaseSync method [DXGI],IDXGIKeyedMutex interface, direct3ddxgi.idxgikeyedmutex_releasesync, dxgi/IDXGIKeyedMutex::ReleaseSync
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIKeyedMutex::ReleaseSync
 - dxgi/IDXGIKeyedMutex::ReleaseSync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIKeyedMutex.ReleaseSync
---

# IDXGIKeyedMutex::ReleaseSync


## -description

Using a key, releases exclusive rendering access to a shared resource.

## -parameters

### -param Key

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

A value that indicates which device to give access to. This method succeeds when the device that currently owns the surface calls the <b>ReleaseSync</b> method using the same value. This value can be any UINT64 value.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful.

If the device attempted to release a keyed mutex that is not valid or owned by the device, <b>ReleaseSync</b> returns E_FAIL.

## -remarks

The <b>ReleaseSync</b> method releases a lock to a surface that is shared between multiple devices.  This method uses a key to determine which device currently has exclusive access to the surface.

When a surface is created using the <b>D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX</b> value of the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag">D3D10_RESOURCE_MISC_FLAG</a> enumeration, 
      you must call the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgikeyedmutex-acquiresync">IDXGIKeyedMutex::AcquireSync</a> method before rendering to the surface.  You must call the <b>ReleaseSync</b> method when you are done 
      rendering to a surface.

After you call the <b>ReleaseSync</b> method, the shared resource is unset from the rendering pipeline. 

To acquire a reference to the keyed mutex object of a shared resource, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the resource and pass in 
      the <b>UUID</b> of the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a> interface.  For more information about acquiring this reference, see the following code example.


#### Examples

<b>Acquiring a Keyed Mutex</b>

The following code example demonstrates how to acquire a lock to a shared resource and how to specify a key upon release.


```

// pDesc has already been set up with texture description.
pDesc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;

// Create a shared texture resource.
pD3D10DeviceD->CreateTexture2D(pDesc, NULL, pD3D10Texture);

// Acquire a reference to the keyed mutex.
pD3D10Texture->QueryInterface(_uuidof(IDXGIKeyedMutex), pDXGIKeyedMutex);

// Acquire a lock to the resource.
pDXGIKeyedMutex->AcquireSync(0, INFINITE);

// Release the lock and specify a key.
pDXGIKeyedMutex->ReleaseSync(1);

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgikeyedmutex-acquiresync">IDXGIKeyedMutex::AcquireSync</a>