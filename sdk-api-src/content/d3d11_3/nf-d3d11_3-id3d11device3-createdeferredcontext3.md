---
UID: NF:d3d11_3.ID3D11Device3.CreateDeferredContext3
title: ID3D11Device3::CreateDeferredContext3 (d3d11_3.h)
description: Creates a deferred context, which can record command lists. (ID3D11Device3.CreateDeferredContext3)
helpviewer_keywords: ["CreateDeferredContext3","CreateDeferredContext3 method [Direct3D 11]","CreateDeferredContext3 method [Direct3D 11]","ID3D11Device3 interface","ID3D11Device3 interface [Direct3D 11]","CreateDeferredContext3 method","ID3D11Device3.CreateDeferredContext3","ID3D11Device3::CreateDeferredContext3","d3d11_3/ID3D11Device3::CreateDeferredContext3","direct3d11.id3d11device3_createdeferredcontext3"]
old-location: direct3d11\id3d11device3_createdeferredcontext3.htm
tech.root: direct3d11
ms.assetid: 78B52E38-3256-4151-96DA-4C81A2A516CF
ms.date: 12/05/2018
ms.keywords: CreateDeferredContext3, CreateDeferredContext3 method [Direct3D 11], CreateDeferredContext3 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateDeferredContext3 method, ID3D11Device3.CreateDeferredContext3, ID3D11Device3::CreateDeferredContext3, d3d11_3/ID3D11Device3::CreateDeferredContext3, direct3d11.id3d11device3_createdeferredcontext3
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device3::CreateDeferredContext3
 - d3d11_3/ID3D11Device3::CreateDeferredContext3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device3.CreateDeferredContext3
---

# ID3D11Device3::CreateDeferredContext3


## -description

Creates a deferred context, which can record <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command lists</a>.

## -parameters

### -param ContextFlags

Type: <b>UINT</b>

Reserved for future use.  Pass 0.

### -param ppDeferredContext [out, optional]

Type: <b>ID3D11DeviceContext3**</b>

Upon completion of the method, the passed pointer to an <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a> interface pointer is initialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
                If this error occurs, you should destroy and recreate the device.
              </li>
<li>Returns <b>DXGI_ERROR_INVALID_CALL</b> if the
               <b>CreateDeferredContext3</b> method can't be called from the current context.
                For example, if the device was created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext3</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
              </li>
<li>Returns <b>E_INVALIDARG</b> if the <i>ContextFlags</i> parameter is invalid.
              </li>
<li>Returns <b>E_OUTOFMEMORY</b> if the app has exhausted available memory.
              </li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdeferredcontext1">ID3D11Device1::CreateDeferredContext1</a>



<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-createdeferredcontext2">ID3D11Device2::CreateDeferredContext2</a>



<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdeferredcontext">ID3D11Device::CreateDeferredContext</a>
