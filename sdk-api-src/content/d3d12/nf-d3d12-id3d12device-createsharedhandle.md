---
UID: NF:d3d12.ID3D12Device.CreateSharedHandle
title: ID3D12Device::CreateSharedHandle (d3d12.h)
description: Creates a shared handle to a heap, resource, or fence object.
helpviewer_keywords: ["CreateSharedHandle","CreateSharedHandle method","CreateSharedHandle method","ID3D12Device interface","ID3D12Device interface","CreateSharedHandle method","ID3D12Device.CreateSharedHandle","ID3D12Device::CreateSharedHandle","d3d12/ID3D12Device::CreateSharedHandle","direct3d12.id3d12device_createsharedhandle"]
old-location: direct3d12\id3d12device_createsharedhandle.htm
tech.root: direct3d12
ms.assetid: AFF058FF-358F-4FF3-8C92-57A9D34B27D9
ms.date: 12/05/2018
ms.keywords: CreateSharedHandle, CreateSharedHandle method, CreateSharedHandle method,ID3D12Device interface, ID3D12Device interface,CreateSharedHandle method, ID3D12Device.CreateSharedHandle, ID3D12Device::CreateSharedHandle, d3d12/ID3D12Device::CreateSharedHandle, direct3d12.id3d12device_createsharedhandle
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CreateSharedHandle
 - d3d12/ID3D12Device::CreateSharedHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateSharedHandle
---

# ID3D12Device::CreateSharedHandle


## -description

Creates a shared handle to a heap, resource, or fence object.

## -parameters

### -param pObject [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a> interface that represents the heap, resource, or fence object to create for sharing.
            The following interfaces (derived from <b>ID3D12DeviceChild</b>) are supported:
            

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12heap">ID3D12Heap</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>
</li>
</ul>

### -param pAttributes [in, optional]

Type: <b>const <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>*</b>

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that contains two separate but related data members: an optional security descriptor, and a <b>Boolean</b> value that determines whether child processes can inherit the returned handle.
            

Set this parameter to <b>NULL</b> if you want child processes that the
              application might create to not  inherit  the handle returned by
              <b>CreateSharedHandle</b>, and if you want the resource that is associated with the returned handle to get a default security
              descriptor.
            

The <b>lpSecurityDescriptor</b> member of the structure specifies a
              <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> for the resource.
              Set this member to <b>NULL</b> if you want the runtime to assign a default security descriptor to the resource that is associated with the returned handle.
              The ACLs in the default security descriptor for the resource come from the primary or impersonation token of the creator.
              For more info, see <a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Synchronization Object Security and Access Rights</a>.

### -param Access

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Currently the only value this parameter accepts is GENERIC_ALL.

### -param Name [in, optional]

Type: <b>LPCWSTR</b>

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name to associate with the shared heap.
              The name is limited to MAX_PATH characters.
              Name comparison is case-sensitive.
            

If <i>Name</i> matches the name of an existing resource, <b>CreateSharedHandle</b> fails with <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NAME_ALREADY_EXISTS</a>.
              This occurs because these objects share the same namespace.
            

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace.
              The remainder of the name can contain any character except the backslash character (\\).
              For more information, see
              <a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.
              Fast user switching is implemented using Terminal Services sessions.
              Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.
            

The object can be created in a private namespace.
              For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

### -param pHandle [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

A pointer to a variable that receives the NT HANDLE value to the resource to share.
            You can use this handle in calls to access the resource.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following values:
              

<ul>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if one of the parameters is invalid.
              </li>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NAME_ALREADY_EXISTS</a> if the supplied name of the resource to share is already associated with another resource.
              </li>
<li>E_ACCESSDENIED if the object is being created in a protected namespace.</li>
<li>E_OUTOFMEMORY if sufficient memory is not available to create the handle.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> topic.
              </li>
</ul>

## -remarks

Both heaps and committed resources can be shared. Sharing a committed resource shares the implicit heap along with the committed resource description, such that a compatible resource description can be mapped to the heap from another device.

For Direct3D 11 and Direct3D 12 interop scenarios, a shared fence is opened in DirectX 11 with the <a href="/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11device5-opensharedfence">ID3D11Device5::OpenSharedFence</a> method, and a shared resource is opened with the <a href="/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1">ID3D11Device::OpenSharedResource1</a> method.

For Direct3D 12, a shared handle is opened with the <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle">ID3D12Device::OpenSharedHandle</a> or the ID3D12Device::OpenSharedHandleByName method.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>

