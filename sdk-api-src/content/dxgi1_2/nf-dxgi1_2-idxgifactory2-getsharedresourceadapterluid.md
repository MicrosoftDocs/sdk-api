---
UID: NF:dxgi1_2.IDXGIFactory2.GetSharedResourceAdapterLuid
title: IDXGIFactory2::GetSharedResourceAdapterLuid
author: windows-sdk-content
description: Identifies the adapter on which a shared resource object was created.
old-location: direct3ddxgi\idxgifactory2_getsharedresourceadapterluid.htm
old-project: direct3ddxgi
ms.assetid: 278F1C2B-6DE7-4D4A-8C6E-10B1004B8EFC
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetSharedResourceAdapterLuid, GetSharedResourceAdapterLuid method [DXGI], GetSharedResourceAdapterLuid method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],GetSharedResourceAdapterLuid method, IDXGIFactory2.GetSharedResourceAdapterLuid, IDXGIFactory2::GetSharedResourceAdapterLuid, direct3ddxgi.idxgifactory2_getsharedresourceadapterluid, dxgi1_2/IDXGIFactory2::GetSharedResourceAdapterLuid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2.GetSharedResourceAdapterLuid
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
<li><a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_INVALID_CALL</a> if <i>hResource</i> is invalid.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.</li>
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
 

 

