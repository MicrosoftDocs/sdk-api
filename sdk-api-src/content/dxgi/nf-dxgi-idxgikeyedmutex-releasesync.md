---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
// pDesc has already been set up with texture description.
pDesc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;

// Create a shared texture resource.
pD3D10DeviceD-&gt;CreateTexture2D(pDesc, NULL, pD3D10Texture);

// Acquire a reference to the keyed mutex.
pD3D10Texture-&gt;QueryInterface(_uuidof(IDXGIKeyedMutex), pDXGIKeyedMutex);

// Acquire a lock to the resource.
pDXGIKeyedMutex-&gt;AcquireSync(0, INFINITE);

// Release the lock and specify a key.
pDXGIKeyedMutex-&gt;ReleaseSync(1);
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a>



<a href="https://msdn.microsoft.com/31edab76-7b16-4a02-83ff-998c21e77f2e">IDXGIKeyedMutex::AcquireSync</a>
 

 

