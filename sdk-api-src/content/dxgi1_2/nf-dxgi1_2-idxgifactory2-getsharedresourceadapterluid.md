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

# IDXGIFactory2::GetSharedResourceAdapterLuid


## -description


Identifies the adapter on which a shared resource object was created.


## -parameters




### -param hResource [in]

A handle to a shared resource object. The <a href="https://msdn.microsoft.com/7A53616A-E7AB-4EB7-9B8F-ED43A70B691C">IDXGIResource1::CreateSharedHandle</a> method returns this handle.


### -param pLuid [out]

A pointer to a variable that receives a locally unique identifier (<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>) value that identifies the adapter. <b>LUID</b> is defined in Dxgi.h. An <b>LUID</b> is a 64-bit value that is guaranteed to be unique only on the operating system on which it was generated. The uniqueness of an <b>LUID</b> is guaranteed only until the operating system is restarted.


## -returns



<b>GetSharedResourceAdapterLuid</b> returns:
        <ul>
<li>S_OK if it  identified the adapter.</li>
<li><a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a> if <i>hResource</i> is invalid.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>GetSharedResourceAdapterLuid</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



You cannot share resources across adapters. Therefore, you cannot open a shared resource on an adapter other than the adapter on which the resource was created.  Call <b>GetSharedResourceAdapterLuid</b> before you open a shared resource to ensure that the resource was created on the appropriate adapter. To open a shared resource, call the <a href="https://msdn.microsoft.com/4751B49E-01DB-467B-879C-743C8B43DDA5">ID3D11Device1::OpenSharedResource1</a> or <a href="https://msdn.microsoft.com/5A7575E4-382E-4A2F-AFE8-2E5850526E75">ID3D11Device1::OpenSharedResourceByName</a> method.


#### Examples

<pre class="syntax" xml:space="preserve"><code>HANDLE handle;
IDXGIFactory2* pFactory;

LUID luid;
pFactory-&gt;GetSharedResourceAdapterLuid (handle, &amp;luid);

UINT index = 0;
IDXGIAdapter* pAdapter = NULL;
while (SUCCEEDED(pFactory-&gt;EnumAdapters(index, &amp;pAdapter)))
{
    DXGI_ADAPTER_DESC desc;
    pAdapter-&gt;GetDesc(&amp;desc);
    if (desc.AdapterLuid == luid)
    {
       // Identified a matching adapter.
       break;
    }
    pAdapter-&gt;Release();
    pAdapter = NULL;
    index++;
}
// At this point, if pAdapter is non-null, you identified an adapter that 
// can open the shared resource.
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

