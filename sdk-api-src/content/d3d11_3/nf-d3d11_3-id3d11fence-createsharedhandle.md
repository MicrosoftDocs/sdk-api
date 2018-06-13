---
UID: NF:d3d11_3.ID3D11Fence.CreateSharedHandle
title: ID3D11Fence::CreateSharedHandle
author: windows-sdk-content
description: Creates a shared handle to a fence object.
old-location: direct3d11\id3d11fence_createsharedhandle.htm
old-project: direct3d11
ms.assetid: 07447C9A-8F69-4FCA-B75C-D7015292F25D
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: CreateSharedHandle, CreateSharedHandle method [Direct3D 11], CreateSharedHandle method [Direct3D 11],ID3D11Fence interface, ID3D11Fence interface [Direct3D 11],CreateSharedHandle method, ID3D11Fence.CreateSharedHandle, ID3D11Fence::CreateSharedHandle, d3d11_3/ID3D11Fence::CreateSharedHandle, direct3d11.id3d11fence_createsharedhandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11Fence.CreateSharedHandle
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
---

# ID3D11Fence::CreateSharedHandle


## -description



          Creates a shared handle to a fence object.
        

This member function is equivalent to the Direct3D 12 <a href="https://msdn.microsoft.com/AFF058FF-358F-4FF3-8C92-57A9D34B27D9">ID3D12Device::CreateSharedHandle</a> member function, and applies between Direct3D 11 and Direct3D 12 in interop scenarios.


## -parameters




### -param pAttributes [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>*</b>


              A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
              structure that contains two separate but related data members: an optional security descriptor, and a <b>Boolean</b>
              value that determines whether child processes can inherit the returned handle.
            


              Set this parameter to <b>NULL</b> if you want child processes that the
              application might create to not  inherit  the handle returned by
              <b>CreateSharedHandle</b>, and if you want the resource that is associated with the returned handle to get a default security
              descriptor.
            


              The <b>lpSecurityDescriptor</b> member of the structure specifies a
              <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> for the resource.
              Set this member to <b>NULL</b> if you want the runtime to assign a default security descriptor to the resource that is associated with the returned handle.
              The ACLs in the default security descriptor for the resource come from the primary or impersonation token of the creator.
              For more info, see <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.
            


### -param dwAccess




### -param lpName




### -param pHandle [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a>*</b>


            A pointer to a variable that receives the NT HANDLE value to the resource to share.
            You can use this handle in calls to access the resource.
          


#### - Access

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Currently the only value this parameter accepts is GENERIC_ALL.


#### - Name [in, optional]

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
<li>
                Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> topic.
              </li>
</ul>



## -remarks



In order to to create a shared handle for the specified fence, the fence must have been created with either the <b>D3D11_FENCE_FLAG_SHARED</b> or <b>D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER</b> flags. For more information see the <a href="direct3d11.d3d11fenceflag">D3D11_FENCE_FLAG</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/DC07EDEF-DA38-4CAF-8FDE-B3867DC83B8C">ID3D11Fence</a>
 

 

