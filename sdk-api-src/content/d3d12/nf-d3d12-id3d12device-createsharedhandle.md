---
UID: NF:d3d12.ID3D12Device.CreateSharedHandle
title: ID3D12Device::CreateSharedHandle
author: windows-sdk-content
description: Creates a shared handle to an heap, resource, or fence object.
old-location: direct3d12\id3d12device_createsharedhandle.htm
tech.root: direct3d12
ms.assetid: AFF058FF-358F-4FF3-8C92-57A9D34B27D9
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CreateSharedHandle, CreateSharedHandle method, CreateSharedHandle method,ID3D12Device interface, ID3D12Device interface,CreateSharedHandle method, ID3D12Device.CreateSharedHandle, ID3D12Device::CreateSharedHandle, d3d12/ID3D12Device::CreateSharedHandle, direct3d12.id3d12device_createsharedhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateSharedHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CreateSharedHandle


## -description


Creates a shared handle to an heap, resource, or fence object.
        


## -parameters




### -param pObject [in]

Type: <b><a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a> interface that represents the heap, resource, or fence object to create for sharing.
            The following interfaces (derived from <b>ID3D12DeviceChild</b>) are supported:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/3791C64F-76D7-4580-A444-F2CEA3EB10CE">ID3D12Heap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2B388352-EF43-4D1E-851C-A670B4681F0F">ID3D12Fence</a>
</li>
</ul>

### -param pAttributes [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>structure that contains two separate but related data members: an optional security descriptor, and a <b>Boolean</b>value that determines whether child processes can inherit the returned handle.
            

Set this parameter to <b>NULL</b> if you want child processes that the
              application might create to not  inherit  the handle returned by
              <b>CreateSharedHandle</b>, and if you want the resource that is associated with the returned handle to get a default security
              descriptor.
            

The <b>lpSecurityDescriptor</b> member of the structure specifies a
              <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> for the resource.
              Set this member to <b>NULL</b> if you want the runtime to assign a default security descriptor to the resource that is associated with the returned handle.
              The ACLs in the default security descriptor for the resource come from the primary or impersonation token of the creator.
              For more info, see <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.
            


### -param Access

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Currently the only value this parameter accepts is GENERIC_ALL.


### -param Name [in, optional]

Type: <b>LPCWSTR</b>

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name to associate with the shared heap.
              The name is limited to MAX_PATH characters.
              Name comparison is case-sensitive.
            

If <i>Name</i> matches the name of an existing resource, <b>CreateSharedHandle</b> fails with <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NAME_ALREADY_EXISTS</a>.
              This occurs because these objects share the same namespace.
            

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace.
              The remainder of the name can contain any character except the backslash character (\).
              For more information, see
              <a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>.
              Fast user switching is implemented using Terminal Services sessions.
              Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.
            

The object can be created in a private namespace.
              For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.
            


### -param pHandle [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

A pointer to a variable that receives the NT HANDLE value to the resource to share.
            You can use this handle in calls to access the resource.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the following values:
              

<ul>
<li><a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a> if one of the parameters is invalid.
              </li>
<li><a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NAME_ALREADY_EXISTS</a> if the supplied name of the resource to share is already associated with another resource.
              </li>
<li>E_ACCESSDENIED if the object is being created in a protected namespace.</li>
<li>E_OUTOFMEMORY if sufficient memory is not available to create the handle.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a> topic.
              </li>
</ul>



## -remarks



Both heaps and committed resources can be shared.
        Sharing a committed resource shares the implicit heap along with the committed resource description, such that a compatible resource description can be mapped to the heap from another device. 
      




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

