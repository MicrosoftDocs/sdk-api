---
UID: NF:dxgi1_2.IDXGIResource1.CreateSharedHandle
title: IDXGIResource1::CreateSharedHandle
author: windows-sdk-content
description: Creates a handle to a shared resource. You can then use the returned handle with multiple Direct3D devices.
old-location: direct3ddxgi\idxgiresource1_createsharedhandle.htm
tech.root: direct3ddxgi
ms.assetid: 7A53616A-E7AB-4EB7-9B8F-ED43A70B691C
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateSharedHandle, CreateSharedHandle method [DXGI], CreateSharedHandle method [DXGI],IDXGIResource1 interface, IDXGIResource1 interface [DXGI],CreateSharedHandle method, IDXGIResource1.CreateSharedHandle, IDXGIResource1::CreateSharedHandle, direct3ddxgi.idxgiresource1_createsharedhandle, dxgi1_2/IDXGIResource1::CreateSharedHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_2.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIResource1.CreateSharedHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIResource1::CreateSharedHandle


## -description


Creates a handle to a shared resource. You can then use the returned handle with multiple Direct3D devices.




## -parameters




### -param pAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
       structure that contains two separate but related data members: an optional security descriptor, and a Boolean 
       value that determines whether child processes can inherit the returned handle.

Set this parameter to <b>NULL</b> if you want child processes that the 
       application might create to not  inherit  the handle returned by 
       <b>CreateSharedHandle</b>, and if you want the resource that is associated with the returned handle to get a default security 
       descriptor.

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> for the resource. Set 
       this member to <b>NULL</b> if you want the runtime to assign a default security descriptor to the resource that is associated with the returned handle. The ACLs in the default security descriptor for the resource come from the primary or impersonation token of the creator. For more info, see <a href="https://msdn.microsoft.com/92478298-617c-4672-a1cc-9a8e9af40327">Synchronization Object Security and Access Rights</a>.


### -param dwAccess [in]

The requested access rights to the resource.  In addition to the <a href="https://msdn.microsoft.com/e18cede9-9bf7-4866-850b-5d7fa43a5b0f">generic access rights</a>, DXGI defines the following values:

<ul>
<li><b>DXGI_SHARED_RESOURCE_READ</b> ( 0x80000000L ) - specifies read access to the resource.</li>
<li><b>DXGI_SHARED_RESOURCE_WRITE</b>	( 1 ) - specifies  write access to the resource.</li>
</ul>
You can combine these values by using a bitwise OR operation.


### -param lpName [in, optional]

The name of the resource to share. The name is limited to MAX_PATH characters. Name comparison is case sensitive. 



						
						You will need the  resource name if you  call the <a href="https://msdn.microsoft.com/5A7575E4-382E-4A2F-AFE8-2E5850526E75">ID3D11Device1::OpenSharedResourceByName</a> method to access the shared resource by name. If you instead  call the <a href="https://msdn.microsoft.com/4751B49E-01DB-467B-879C-743C8B43DDA5">ID3D11Device1::OpenSharedResource1</a> method to access the shared resource by handle, set this parameter to <b>NULL</b>.

If <i>lpName</i> matches the name of an existing resource, <b>CreateSharedHandle</b> fails with <a href="dxgi_error.htm">DXGI_ERROR_NAME_ALREADY_EXISTS</a>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>. Fast user switching is implemented using Terminal Services sessions. Kernel object names must follow the guidelines outlined for Terminal Services so that applications can support multiple users.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.


### -param pHandle [out]

A pointer to a variable that receives the NT HANDLE value to the resource to share.  You can  use this handle in calls to access the resource.


## -returns



Returns S_OK if successful; otherwise, returns one of the following values:

<ul>
<li><a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a> if one of the parameters is invalid.</li>
<li><a href="dxgi_error.htm">DXGI_ERROR_NAME_ALREADY_EXISTS</a> if the supplied name of the resource to share is already associated with another resource.</li>
<li>E_ACCESSDENIED if the object is being created in a protected namespace.</li>
<li>E_OUTOFMEMORY if sufficient memory is not available to create the handle.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic. </li>
</ul>
<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>CreateSharedHandle</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



<b>CreateSharedHandle</b> only returns the NT handle when you  created the resource as shared and specified that it uses NT handles (that is, you set the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> and <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX</a> flags). If you  created the resource as shared and specified that it uses NT handles, you must use <b>CreateSharedHandle</b> to get a handle for sharing.  In this situation, you can't use the <a href="https://msdn.microsoft.com/7fa92667-2e37-498b-994b-7c576754b86b">IDXGIResource::GetSharedHandle</a> method because it will fail.

You can pass the handle that  <b>CreateSharedHandle</b> returns in a call to the <a href="https://msdn.microsoft.com/4751B49E-01DB-467B-879C-743C8B43DDA5">ID3D11Device1::OpenSharedResource1</a> method to give a device access to a shared resource that you created on a different device.

Because the handle that  <b>CreateSharedHandle</b> returns is an NT handle, you can use the handle with <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>, <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, and so on. You can call <b>CreateSharedHandle</b> only once for a shared resource; later calls fail.  If you need more handles to the same shared resource, call <b>DuplicateHandle</b>. When you no longer need the shared resource handle, call <b>CloseHandle</b> to close the handle, in order to avoid memory leaks.

If you pass a name for the resource to <i>lpName</i> when you call <b>CreateSharedHandle</b> to share the resource, you can subsequently pass this name in a call to the <a href="https://msdn.microsoft.com/5A7575E4-382E-4A2F-AFE8-2E5850526E75">ID3D11Device1::OpenSharedResourceByName</a> method to give another device access to the shared resource. If you use a named resource, a malicious user can use this named resource before you do and prevent your app from starting. To prevent this situation, create a randomly named resource and store the name so that it can only be obtained by an authorized user. Alternatively, you can use a file for this purpose. To limit your app to one instance per user, create a locked file in the user's profile directory.

If you  created the resource as shared and did not specify that it uses NT handles, you cannot use <b>CreateSharedHandle</b> to get a handle for sharing because <b>CreateSharedHandle</b> will fail.


#### Examples

<pre class="syntax" xml:space="preserve"><code>ID3D11Texture2D* pTexture2D;
ID3D11Device* pDevice;

pDevice-&gt;CreateTexture2D(…, &amp;pTexture2D); // Create the texture as shared with NT HANDLEs.

HANDLE handle;
IDXGIResource1* pResource;
pTexture2D-&gt;QueryInterface(__uuidof(IDXGIResource1), (void**) &amp;pResource);
pResource-&gt;CreateSharedHandle(NULL, 
         DXGI_SHARED_REOUSRCE_READ | DXGI_SHARED_RESOURCE_WRITE, 
         NULL,
         &amp;handle);

// Pass the handle to another process to share the resource.
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/0ABA9B8D-BEA4-4455-A312-7CFEDEBBF19A">IDXGIResource1</a>
 

 

