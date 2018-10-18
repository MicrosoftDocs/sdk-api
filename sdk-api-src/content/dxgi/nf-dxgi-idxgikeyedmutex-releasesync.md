---
UID: NF:dxgi.IDXGIKeyedMutex.ReleaseSync
title: IDXGIKeyedMutex::ReleaseSync
author: windows-sdk-content
description: Using a key, releases exclusive rendering access to a shared resource.
old-location: direct3ddxgi\idxgikeyedmutex_releasesync.htm
tech.root: direct3ddxgi
ms.assetid: 324741c9-33f2-4420-8c3f-4984e2ca0962
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 33872a53-bb15-32f2-c1f4-cfc8bdbac157, IDXGIKeyedMutex interface [DXGI],ReleaseSync method, IDXGIKeyedMutex.ReleaseSync, IDXGIKeyedMutex::ReleaseSync, ReleaseSync, ReleaseSync method [DXGI], ReleaseSync method [DXGI],IDXGIKeyedMutex interface, direct3ddxgi.idxgikeyedmutex_releasesync, dxgi/IDXGIKeyedMutex::ReleaseSync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIKeyedMutex::ReleaseSync


## -description


Using a key, releases exclusive rendering access to a shared resource.


## -parameters




### -param Key

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

A value that indicates which device to give access to. This method succeeds when the device that currently owns the surface calls the <b>ReleaseSync</b> method using the same value. This value can be any UINT64 value.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful.

If the device attempted to release a keyed mutex that is not valid or owned by the device, <b>ReleaseSync</b> returns E_FAIL.




## -remarks



The <b>ReleaseSync</b> method releases a lock to a surface that is shared between multiple devices.  This method uses a key to determine which device currently has exclusive access to the surface.

When a surface is created using the <b>D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX</b> value of the <a href="https://msdn.microsoft.com/bdcb4e87-0285-4e96-a7ce-e08a43d3a4cb">D3D10_RESOURCE_MISC_FLAG</a> enumeration, 
      you must call the <a href="https://msdn.microsoft.com/31edab76-7b16-4a02-83ff-998c21e77f2e">IDXGIKeyedMutex::AcquireSync</a> method before rendering to the surface.  You must call the <b>ReleaseSync</b> method when you are done 
      rendering to a surface.

After you call the <b>ReleaseSync</b> method, the shared resource is unset from the rendering pipeline. 

To acquire a reference to the keyed mutex object of a shared resource, call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of the resource and pass in 
      the <b>UUID</b> of the <a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a> interface.  For more information about acquiring this reference, see the following code example.


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




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a>



<a href="https://msdn.microsoft.com/31edab76-7b16-4a02-83ff-998c21e77f2e">IDXGIKeyedMutex::AcquireSync</a>
 

 

