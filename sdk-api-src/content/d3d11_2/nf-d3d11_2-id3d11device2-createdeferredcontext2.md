---
UID: NF:d3d11_2.ID3D11Device2.CreateDeferredContext2
title: ID3D11Device2::CreateDeferredContext2 (d3d11_2.h)
description: Creates a deferred context, which can record command lists. (ID3D11Device2.CreateDeferredContext2)
helpviewer_keywords: ["CreateDeferredContext2","CreateDeferredContext2 method [Direct3D 11]","CreateDeferredContext2 method [Direct3D 11]","ID3D11Device2 interface","ID3D11Device2 interface [Direct3D 11]","CreateDeferredContext2 method","ID3D11Device2.CreateDeferredContext2","ID3D11Device2::CreateDeferredContext2","d3d11_2/ID3D11Device2::CreateDeferredContext2","direct3d11.id3d11device2_createdeferredcontext2"]
old-location: direct3d11\id3d11device2_createdeferredcontext2.htm
tech.root: direct3d11
ms.assetid: 57901FAC-428C-437B-9C9B-2DB2D16049F8
ms.date: 12/05/2018
ms.keywords: CreateDeferredContext2, CreateDeferredContext2 method [Direct3D 11], CreateDeferredContext2 method [Direct3D 11],ID3D11Device2 interface, ID3D11Device2 interface [Direct3D 11],CreateDeferredContext2 method, ID3D11Device2.CreateDeferredContext2, ID3D11Device2::CreateDeferredContext2, d3d11_2/ID3D11Device2::CreateDeferredContext2, direct3d11.id3d11device2_createdeferredcontext2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device2::CreateDeferredContext2
 - d3d11_2/ID3D11Device2::CreateDeferredContext2
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
 - ID3D11Device2.CreateDeferredContext2
---

# ID3D11Device2::CreateDeferredContext2


## -description

Creates a deferred context, which can record <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command lists</a>.

## -parameters

### -param ContextFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reserved for future use.
            Pass 0.

### -param ppDeferredContext [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a>**</b>

Upon completion of the method, the passed pointer to an <a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContext2</a> interface pointer is initialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following:
            

<ul>
<li>Returns <b>DXGI_ERROR_DEVICE_REMOVED</b> if the video card has been physically removed from the system, or a driver upgrade for the video card has occurred.
                If this error occurs, you should destroy and recreate the device.
              </li>
<li>Returns <b>DXGI_ERROR_INVALID_CALL</b> if the <b>CreateDeferredContext2</b> method can't be called from the current context.
                For example, if the device was created with the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value,  <b>CreateDeferredContext2</b> returns <b>DXGI_ERROR_INVALID_CALL</b>.
              </li>
<li>Returns <b>E_INVALIDARG</b> if the <i>ContextFlags</i> parameter is invalid.
              </li>
<li>Returns <b>E_OUTOFMEMORY</b> if the app has exhausted available memory.
              </li>
</ul>

## -remarks

A deferred context is a thread-safe context that you can use to record graphics commands on a thread other than the main rendering thread.
          By using a deferred context, you can record graphics commands into a command list that is encapsulated by the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11commandlist">ID3D11CommandList</a> interface.
          After you record all scene items, you can then submit them to the main render thread for final rendering.
          In this manner, you can perform rendering tasks concurrently across multiple threads and potentially improve performance in multi-core CPU scenarios.
        

You can create multiple deferred contexts.
        

<div class="alert"><b>Note</b>  If you use the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_SINGLETHREADED</a> value to create the device,
          <b>CreateDeferredContext2</b> fails with <b>DXGI_ERROR_INVALID_CALL</b>, and you can't create a deferred context.
        </div>
<div> </div>
For more information about deferred contexts, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render">Immediate and Deferred Rendering</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-createdeferredcontext1">ID3D11Device1::CreateDeferredContext1</a>



<a href="/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2">ID3D11Device2</a>



<a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createdeferredcontext3">ID3D11Device3::CreateDeferredContext3</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdeferredcontext">ID3D11Device::CreateDeferredContext</a>
