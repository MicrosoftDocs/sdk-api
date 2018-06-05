---
UID: NF:dxgi1_5.IDXGIDevice4.OfferResources1
title: IDXGIDevice4::OfferResources1
author: windows-sdk-content
description: Allows the operating system to free the video memory of resources, including both discarding the content and de-committing the memory.
old-location: direct3ddxgi\idxgidevice4_offerresources1.htm
old-project: direct3ddxgi
ms.assetid: 7F6782F3-7779-4DBD-AD5A-AE0FB136FC70
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIDevice4 interface [DXGI],OfferResources1 method, IDXGIDevice4.OfferResources1, IDXGIDevice4::OfferResources1, OfferResources1, OfferResources1 method [DXGI], OfferResources1 method [DXGI],IDXGIDevice4 interface, direct3ddxgi.idxgidevice4_offerresources1, dxgi1_5/IDXGIDevice4::OfferResources1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_5.h
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
req.typenames: DXGI_RECLAIM_RESOURCE_RESULTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxgi.dll
api_name:
-	IDXGIDevice4.OfferResources1
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice4::OfferResources1


## -description


Allows the operating system to free the video memory of resources, including both discarding the content and de-committing the memory.


## -parameters




### -param NumResources [in]

Type: <b>UINT</b>

The number of resources in the <i>ppResources</i> argument array.


### -param ppResources [in]

Type: <b>IDXGIResource*</b>

An array of pointers to <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> interfaces for the resources to offer.


### -param Priority [in]

Type: <b>DXGI_OFFER_RESOURCE_PRIORITY</b>

A <a href="https://msdn.microsoft.com/BDC0AAA3-2B72-4732-82CE-458C14B0D993">DXGI_OFFER_RESOURCE_PRIORITY</a>-typed value that indicates how valuable data is.


### -param Flags [in]

Type: <b>UINT</b>

Specifies the <a href="https://msdn.microsoft.com/55107136-60C0-49E9-8DD1-24878E67FCBB">DXGI_OFFER_RESOURCE_FLAGS</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if a resource in the array, or the priority, is invalid.




## -remarks



<b>OfferResources1</b> (an extension of the original <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a> API) enables D3D based applications to allow de-committing of an allocation’s backing store to reduce system commit under low memory conditions. 
A de-committed allocation cannot be reused, so opting in to the new DXGI_OFFER_RESOURCE_FLAG_ALLOW_DECOMMIT flag means the new reclaim results must be properly handled. Refer to the flag descriptions in <a href="https://msdn.microsoft.com/AF7082A5-6280-4602-9944-EC2DFF91BBB9">DXGI_RECLAIM_RESOURCE_RESULTS</a> and the Example below.

<b>OfferResources1</b> and <a href="https://msdn.microsoft.com/83D09C41-CB96-4ADA-AE38-7D9542CCCFE0">ReclaimResources1</a> may <i>not</i> be used interchangeably with <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">OfferResources</a> and <a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a>. 


The priority value that the  <i>Priority</i> parameter specifies describes how valuable the caller considers the content to be.  The operating system uses the priority value to discard resources in order of priority. The operating system discards a resource that is offered with low priority before it discards a resource that is  offered with a higher priority.

If you call <b>OfferResources1</b> to offer a resource while the resource is bound to the pipeline, the resource is unbound.  You cannot call <b>OfferResources1</b> on a resource that is mapped.  After you offer a resource, the resource cannot be mapped or bound to the pipeline until you call the <a href="https://msdn.microsoft.com/83D09C41-CB96-4ADA-AE38-7D9542CCCFE0">ReclaimResources1</a> method to reclaim the resource. You cannot call <b>OfferResources1</b> to offer immutable resources.

To offer shared resources, call <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">OfferResources1</a> on only one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a> object and then call <b>OfferResources1</b> only while you hold the mutex. In fact, you can't offer shared resources unless you use <b>IDXGIKeyedMutex</b> because offering shared resources without using <b>IDXGIKeyedMutex</b> isn't supported.

The user mode display driver might not immediately offer the resources that you specified in a call to <b>OfferResources1</b>. The driver can postpone offering them until the next call to <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>, <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a>, or <a href="https://msdn.microsoft.com/e204c585-4996-4274-a654-b9912e957fe6">ID3D11DeviceContext::Flush</a>.


#### Examples

A UWP based application is being suspended to the background and wishes to offer its graphics resources back to the system, in case another application wants them. The application will reclaim these resources when it gets resumed. The application also realizes that the total available system commit is small on this platform, and is willing to allow its resources to be removed from the system commit. If the reclaim process fails because the system is out of memory, the application handles the error condition.  


<pre class="syntax" xml:space="preserve"><code>struct Texture 
{ 
    UINT32 Width; 
    UINT32 Height; 
    UINT32 Mips; 
    ID3D11Texture2D* pResource; 
};  

void Application::OfferInterfaceResources(ID3D11Device* pD3D11Device) 
{ 
    CComPtr&lt;IDXGIDevice4&gt; pDXGIDevice; 
    ThrowIfFailed(pD3D11Device-&gt;QueryInterface(&amp;pDXGIDevice)); 

    for(Texture&amp; t : m_Textures) 
    { 
        CComPtr&lt;IDXGIResource&gt; pDXGIResource; 
        ThrowIfFailed(t.pResource-&gt;QueryInterface(&amp;pDXGIResource));   
        ThrowIfFailed(pDXGIDevice-&gt;OfferResources1(1, &amp;pDXGIResource, DXGI_OFFER_RESOURCE_PRIORITY_NORMAL, 
											DXGI_OFFER_RESOURCE_FLAG_ALLOW_DECOMMIT)); 
    } 
} 

void Application::ReclaimInterfaceResources (ID3D11Device* pD3D11Device) 
{ 
    CComPtr&lt;IDXGIDevice4&gt; pDXGIDevice; 
    ThrowIfFailed(pD3D11Device-&gt;QueryInterface(&amp;pDXGIDevice));  

    for(Texture&amp; t : m_Textures) 
    { 
        CComPtr&lt;IDXGIResource&gt; pDXGIResource; 
        ThrowIfFailed(t.pResource-&gt;QueryInterface(&amp;pDXGIResource));       

        DXGI_RECLAIM_RESOURCE_RESULTS Result; 
        ThrowIfFailed(pDXGIDevice-&gt;ReclaimResources1(1, &amp;pDXGIResource, &amp;Result)); 

        // If the surface lost its backing commitment, it must be recreated. 

        if(Result == DXGI_RECLAIM_RESOURCE_RESULT_NOT_COMMITTED) 
        { 
            t.pResource-&gt;Release(); 
            t.pResource = CreateTexture(t.Width, t.Height, t.Mips); 
        }  

        // If the surface lost its content (either because it was discarded, or recreated 
        // due to lost commitment), we must regenerate the content. 

        if(Result != DXGI_RECLAIM_RESOURCE_RESULT_OK) 
        { 
            PopulateContent(t); 
        } 
    } 
} 
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/AF7082A5-6280-4602-9944-EC2DFF91BBB9">DXGI_RECLAIM_RESOURCE_RESULTS</a>



<a href="https://msdn.microsoft.com/15EA6B68-587E-4D92-A70D-7DDA9915EBC2">IDXGIDevice4</a>
 

 

