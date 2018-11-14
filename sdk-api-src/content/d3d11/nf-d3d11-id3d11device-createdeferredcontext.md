---
UID: NF:d3d11.ID3D11Device.CreateDeferredContext
title: ID3D11Device::CreateDeferredContext
author: windows-sdk-content
description: Creates a deferred context, which can record command lists.
old-location: direct3d11\id3d11device_createdeferredcontext.htm
tech.root: direct3d11
ms.assetid: fbf01844-eaf1-4360-833e-c95ba686fff5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateDeferredContext, CreateDeferredContext method [Direct3D 11], CreateDeferredContext method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateDeferredContext method, ID3D11Device.CreateDeferredContext, ID3D11Device::CreateDeferredContext, ad59e9e8-de25-e887-81b2-63e050b34473, d3d11/ID3D11Device::CreateDeferredContext, direct3d11.id3d11device_createdeferredcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
 - ID3D11Device.CreateDeferredContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11Device.CreateDeferredContext
: 
---

# ID3D11Device::CreateDeferredContext


## -description


Creates a deferred context, which can record command lists.


## -parameters




### -param ContextFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Reserved for future use.
            Pass 0.
          


### -param ppDeferredContext [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>**</b>

Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a> interface pointer is initialized.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
                If this error occurs, you should destroy and recreate the device.
              </li>
<li>Returns <b>DXGI_ERROR_INVALID_CALL</b> if the <b>CreateDeferredContext</b> method cannot be called from the current context.
                For example, if the device was created with the <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
              </li>
<li>Returns <b>E_INVALIDARG</b> if the <i>ContextFlags</i> parameter is invalid.
              </li>
<li>Returns <b>E_OUTOFMEMORY</b> if the application has exhausted available memory.
              </li>
</ul>



## -remarks



A deferred context is a thread-safe context that you can use to record graphics commands on a thread other than the main rendering thread.
          Using a deferred context, you can record graphics commands into a command list that is encapsulated by the <a href="https://msdn.microsoft.com/en-us/library/Ff476361(v=VS.85).aspx">ID3D11CommandList</a> interface.
          After all scene items are recorded, you can then submit them to the main render thread for final rendering.
          In this manner, you can perform rendering tasks concurrently across multiple threads and potentially improve performance in multi-core CPU scenarios.
        

You can create multiple deferred contexts.
        

<div class="alert"><b>Note</b>  If you use the <a href="https://msdn.microsoft.com/en-us/library/Ff476107(v=VS.85).aspx">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value to create the device that is represented by <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>, the <b>CreateDeferredContext</b> method will fail, and you will not be able to create a deferred context.
        </div>
<div> </div>
For more information about deferred contexts, see <a href="https://msdn.microsoft.com/en-us/library/Ff476892(v=VS.85).aspx">Immediate and Deferred Rendering</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404580(v=VS.85).aspx">ID3D11Device1::CreateDeferredContext1</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn280495(v=VS.85).aspx">ID3D11Device2::CreateDeferredContext2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn912871(v=VS.85).aspx">ID3D11Device3::CreateDeferredContext3</a>
 

 

