---
UID: NF:dxgi.IDXGIResource.GetSharedHandle
title: IDXGIResource::GetSharedHandle (dxgi.h)
description: Gets the handle to a shared resource.
helpviewer_keywords: ["GetSharedHandle","GetSharedHandle method [DXGI]","GetSharedHandle method [DXGI]","IDXGIResource interface","IDXGIResource interface [DXGI]","GetSharedHandle method","IDXGIResource.GetSharedHandle","IDXGIResource::GetSharedHandle","direct3ddxgi.idxgiresource_getsharedhandle","dxgi/IDXGIResource::GetSharedHandle","fea59fdb-2526-c2b6-2bd7-58a9fe56c221"]
old-location: direct3ddxgi\idxgiresource_getsharedhandle.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource_getsharedhandle.htm
ms.date: 12/05/2018
ms.keywords: GetSharedHandle, GetSharedHandle method [DXGI], GetSharedHandle method [DXGI],IDXGIResource interface, IDXGIResource interface [DXGI],GetSharedHandle method, IDXGIResource.GetSharedHandle, IDXGIResource::GetSharedHandle, direct3ddxgi.idxgiresource_getsharedhandle, dxgi/IDXGIResource::GetSharedHandle, fea59fdb-2526-c2b6-2bd7-58a9fe56c221
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
 - IDXGIResource::GetSharedHandle
 - dxgi/IDXGIResource::GetSharedHandle
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
 - IDXGIResource.GetSharedHandle
---

# IDXGIResource::GetSharedHandle


## -description

<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetSharedHandle</b> anymore to retrieve the handle to a shared resource. Instead, use <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle">IDXGIResource1::CreateSharedHandle</a> to get a handle for sharing. To use <b>IDXGIResource1::CreateSharedHandle</b>, you  must create the resource as shared and specify that it uses NT handles (that is, you set the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag). We also recommend that you create shared resources that use NT handles so you can use <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>, <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, and so on on those shared resources.]

Gets the handle to a shared resource.

## -parameters

### -param pSharedHandle [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

A pointer to a handle.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

<b>GetSharedHandle</b> returns a handle for the resource that you created as shared (that is, you set the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED</a> with or without the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX</a> flag). You can pass this handle to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-opensharedresource">ID3D11Device::OpenSharedResource</a> method to give another device access to the shared resource. You can also marshal this handle to another process to share a resource with a device in another process. However, this handle is not an NT handle. Therefore, don't use the handle with <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>, <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, and so on.

The creator of a shared resource must not destroy the resource until all intended entities have opened the resource. The validity of the handle is tied to the lifetime of the underlying video memory. If no resource objects exist on any devices that refer to this resource, the handle is no longer valid. To extend the lifetime of the handle and video memory, you must open the shared resource on a device.

<b>GetSharedHandle</b> can also return handles for resources that were passed into <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-opensharedresource">ID3D11Device::OpenSharedResource</a> to open those resources.

<b>GetSharedHandle</b> fails if the resource to which it wants to get a handle is not shared.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a>