---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11Device1::OpenSharedResource1


## -description


Gives a device access to a shared resource that is referenced by a handle and that was created on a different device. You must have previously created the resource as shared and specified that it uses NT handles (that is, you set the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag).


## -parameters




### -param hResource [in]

A handle to the resource to open. For more info about this parameter, see Remarks.


### -param returnedInterface [in]

The globally unique identifier (GUID) for the resource interface. For more info about this parameter, see Remarks.


### -param ppResource [out]

A pointer to a variable that receives a pointer to the interface for the shared resource object to access.


## -returns



This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>. This method also returns E_ACCESSDENIED if the permissions to access the resource aren't valid.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>OpenSharedResource1</b> fails with E_NOTIMPL because NTHANDLES are used. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



The behavior of <b>OpenSharedResource1</b> is similar to the behavior of the <a href="https://msdn.microsoft.com/bc054547-e098-457e-8c8a-a41496234a63">ID3D11Device::OpenSharedResource</a> method; each call to <b>OpenSharedResource1</b> to access a resource creates a new resource object.  In other words, if you call <b>OpenSharedResource1</b> twice and pass the same resource handle to <i>hResource</i>, you receive two resource  objects with different <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointers.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To share a resource between two devices</b>

<ol>
<li>Create the resource as shared and specify that it uses NT handles, by setting the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag.</li>
<li>Obtain the REFIID, or GUID, of the interface to the resource by using the __uuidof() macro. For example, __uuidof(<a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a>) retrieves the GUID of the interface to a 2D texture.</li>
<li>Query the resource for the <a href="https://msdn.microsoft.com/0ABA9B8D-BEA4-4455-A312-7CFEDEBBF19A">IDXGIResource1</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/7A53616A-E7AB-4EB7-9B8F-ED43A70B691C">IDXGIResource1::CreateSharedHandle</a> method to obtain the unique handle to the resource.</li>
</ol>

#### Examples

<pre class="syntax" xml:space="preserve"><code>HANDLE handle = GetSharedHandleFromOtherProcess();
ID3D11Device1* pDevice;
ID3D11Texture2D* pTexture2D;

pDevice-&gt;OpenSharedResource1(
          handle, 
          __uuidof(ID3D11Texture2D), 
         (void**)&amp;pTexture2D);
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/DB4DAD13-3CD7-4362-950B-6403328CB071">ID3D11Device1</a>
 

 

