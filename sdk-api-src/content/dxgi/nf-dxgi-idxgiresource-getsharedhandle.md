---
UID: NF:dxgi.IDXGIResource.GetSharedHandle
title: IDXGIResource::GetSharedHandle
author: windows-sdk-content
description: Gets the handle to a shared resource.
old-location: direct3ddxgi\idxgiresource_getsharedhandle.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource_getsharedhandle.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetSharedHandle, GetSharedHandle method [DXGI], GetSharedHandle method [DXGI],IDXGIResource interface, IDXGIResource interface [DXGI],GetSharedHandle method, IDXGIResource.GetSharedHandle, IDXGIResource::GetSharedHandle, direct3ddxgi.idxgiresource_getsharedhandle, dxgi/IDXGIResource::GetSharedHandle, fea59fdb-2526-c2b6-2bd7-58a9fe56c221
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
 - IDXGIResource.GetSharedHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIResource::GetSharedHandle


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetSharedHandle</b> anymore to retrieve the handle to a shared resource. Instead, use <a href="https://msdn.microsoft.com/7A53616A-E7AB-4EB7-9B8F-ED43A70B691C">IDXGIResource1::CreateSharedHandle</a> to get a handle for sharing. To use <b>IDXGIResource1::CreateSharedHandle</b>, you  must create the resource as shared and specify that it uses NT handles (that is, you set the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag). We also recommend that you create shared resources that use NT handles so you can use <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>, <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, and so on on those shared resources.]

Gets the handle to a shared resource.


## -parameters




### -param pSharedHandle [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

A pointer to a handle.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> values.




## -remarks



<b>GetSharedHandle</b> returns a handle for the resource that you created as shared (that is, you set the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED</a> with or without the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX</a> flag). You can pass this handle to the <a href="https://msdn.microsoft.com/bc054547-e098-457e-8c8a-a41496234a63">ID3D11Device::OpenSharedResource</a> method to give another device access to the shared resource. You can also marshal this handle to another process to share a resource with a device in another process. However, this handle is not an NT handle. Therefore, don't use the handle with <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>, <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, and so on.

The creator of a shared resource must not destroy the resource until all intended entities have opened the resource. The validity of the handle is tied to the lifetime of the underlying video memory. If no resource objects exist on any devices that refer to this resource, the handle is no longer valid. To extend the lifetime of the handle and video memory, you must open the shared resource on a device.

<b>GetSharedHandle</b> can also return handles for resources that were passed into <a href="https://msdn.microsoft.com/bc054547-e098-457e-8c8a-a41496234a63">ID3D11Device::OpenSharedResource</a> to open those resources.

<b>GetSharedHandle</b> fails if the resource to which it wants to get a handle is not shared.




## -see-also




<a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a>
 

 

