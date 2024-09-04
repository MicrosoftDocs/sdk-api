---
UID: NF:d3d11_1.ID3D11Device1.OpenSharedResource1
title: ID3D11Device1::OpenSharedResource1 (d3d11_1.h)
description: Gives a device access to a shared resource that is referenced by a handle and that was created on a different device.
helpviewer_keywords: ["ID3D11Device1 interface [Direct3D 11]","OpenSharedResource1 method","ID3D11Device1.OpenSharedResource1","ID3D11Device1::OpenSharedResource1","OpenSharedResource1","OpenSharedResource1 method [Direct3D 11]","OpenSharedResource1 method [Direct3D 11]","ID3D11Device1 interface","d3d11_1/ID3D11Device1::OpenSharedResource1","direct3d11.id3d11device1_opensharedresource1"]
old-location: direct3d11\id3d11device1_opensharedresource1.htm
tech.root: direct3d11
ms.assetid: 4751B49E-01DB-467B-879C-743C8B43DDA5
ms.date: 12/05/2018
ms.keywords: ID3D11Device1 interface [Direct3D 11],OpenSharedResource1 method, ID3D11Device1.OpenSharedResource1, ID3D11Device1::OpenSharedResource1, OpenSharedResource1, OpenSharedResource1 method [Direct3D 11], OpenSharedResource1 method [Direct3D 11],ID3D11Device1 interface, d3d11_1/ID3D11Device1::OpenSharedResource1, direct3d11.id3d11device1_opensharedresource1
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11Device1::OpenSharedResource1
 - d3d11_1/ID3D11Device1::OpenSharedResource1
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
 - ID3D11Device1.OpenSharedResource1
---

# ID3D11Device1::OpenSharedResource1


## -description

Gives a device access to a shared resource that is referenced by a handle and that was created on a different device. You must have previously created the resource as shared and specified that it uses NT handles (that is, you set the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag).

## -parameters

### -param hResource [in]

A handle to the resource to open. For more info about this parameter, see Remarks.

### -param returnedInterface [in]

The globally unique identifier (GUID) for the resource interface. For more info about this parameter, see Remarks.

### -param ppResource [out]

A pointer to a variable that receives a pointer to the interface for the shared resource object to access.

## -returns

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>. This method also returns E_ACCESSDENIED if the permissions to access the resource aren't valid.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>OpenSharedResource1</b> fails with E_NOTIMPL because NTHANDLES are used. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

The behavior of <b>OpenSharedResource1</b> is similar to the behavior of the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-opensharedresource">ID3D11Device::OpenSharedResource</a> method; each call to <b>OpenSharedResource1</b> to access a resource creates a new resource object.  In other words, if you call <b>OpenSharedResource1</b> twice and pass the same resource handle to <i>hResource</i>, you receive two resource  objects with different <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers.

<p class="proch"><b>To share a resource between two devices</b>

<ol>
<li>Create the resource as shared and specify that it uses NT handles, by setting the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag.</li>
<li>Obtain the REFIID, or GUID, of the interface to the resource by using the __uuidof() macro. For example, __uuidof(<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a>) retrieves the GUID of the interface to a 2D texture.</li>
<li>Query the resource for the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1">IDXGIResource1</a> interface.</li>
<li>Call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle">IDXGIResource1::CreateSharedHandle</a> method to obtain the unique handle to the resource.</li>
</ol>

#### Examples


``` syntax
HANDLE handle = GetSharedHandleFromOtherProcess();
ID3D11Device1* pDevice;
ID3D11Texture2D* pTexture2D;

pDevice->OpenSharedResource1(
          handle, 
          __uuidof(ID3D11Texture2D), 
          (void**)&pTexture2D);
```


## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>
