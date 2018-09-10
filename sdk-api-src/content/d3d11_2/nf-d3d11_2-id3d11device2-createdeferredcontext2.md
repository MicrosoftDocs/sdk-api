---
UID: NF:d3d11_2.ID3D11Device2.CreateDeferredContext2
title: ID3D11Device2::CreateDeferredContext2
author: windows-sdk-content
description: Creates a deferred context, which can record command lists.
old-location: direct3d11\id3d11device2_createdeferredcontext2.htm
tech.root: direct3d11
ms.assetid: 57901FAC-428C-437B-9C9B-2DB2D16049F8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateDeferredContext2, CreateDeferredContext2 method [Direct3D 11], CreateDeferredContext2 method [Direct3D 11],ID3D11Device2 interface, ID3D11Device2 interface [Direct3D 11],CreateDeferredContext2 method, ID3D11Device2.CreateDeferredContext2, ID3D11Device2::CreateDeferredContext2, d3d11_2/ID3D11Device2::CreateDeferredContext2, direct3d11.id3d11device2_createdeferredcontext2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ID3D11Device2.CreateDeferredContext2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device2::CreateDeferredContext2


## -description


Creates a deferred context, which can record <a href="https://msdn.microsoft.com/4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e">command lists</a>.
        


## -parameters




### -param ContextFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Reserved for future use.
            Pass 0.
          


### -param ppDeferredContext [out, optional]

Type: <b><a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>**</b>

Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a> interface pointer is initialized.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
                If this error occurs, you should destroy and recreate the device.
              </li>
<li>Returns <b>DXGI_ERROR_INVALID_CALL</b> if the <b>CreateDeferredContext2</b> method can't be called from the current context.
                For example, if the device was created with the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext2</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
              </li>
<li>Returns <b>E_INVALIDARG</b> if the <i>ContextFlags</i> parameter is invalid.
              </li>
<li>Returns <b>E_OUTOFMEMORY</b> if the app has exhausted available memory.
              </li>
</ul>



## -remarks



A deferred context is a thread-safe context that you can use to record graphics commands on a thread other than the main rendering thread.
          By using a deferred context, you can record graphics commands into a command list that is encapsulated by the <a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a> interface.
          After you record all scene items, you can then submit them to the main render thread for final rendering.
          In this manner, you can perform rendering tasks concurrently across multiple threads and potentially improve performance in multi-core CPU scenarios.
        

You can create multiple deferred contexts.
        

<div class="alert"><b>Note</b>  If you use the <a href="https://msdn.microsoft.com/580c784a-17de-495c-9159-833f858ad155">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value to create the device,
          <b>CreateDeferredContext2</b> fails with <b>DXGI_ERROR_INVALID_CALL</b>, and you can't create a deferred context.
        </div>
<div> </div>
For more information about deferred contexts, see <a href="https://msdn.microsoft.com/8991be9f-c882-4752-9048-704fe4ae1725">Immediate and Deferred Rendering</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/2F7E343F-2A25-44F2-9352-5F378718D6F6">ID3D11Device1::CreateDeferredContext1</a>



<a href="https://msdn.microsoft.com/C476AA0E-4A49-4E1E-8308-FB72EAD3E30C">ID3D11Device2</a>



<a href="https://msdn.microsoft.com/78B52E38-3256-4151-96DA-4C81A2A516CF">ID3D11Device3::CreateDeferredContext3</a>



<a href="https://msdn.microsoft.com/fbf01844-eaf1-4360-833e-c95ba686fff5">ID3D11Device::CreateDeferredContext</a>
 

 

