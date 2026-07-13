---
UID: NF:dxgi1_5.IDXGIDevice4.OfferResources1
title: IDXGIDevice4::OfferResources1 (dxgi1_5.h)
description: Allows the operating system to free the video memory of resources, including both discarding the content and de-committing the memory.
helpviewer_keywords: ["IDXGIDevice4 interface [DXGI]","OfferResources1 method","IDXGIDevice4.OfferResources1","IDXGIDevice4::OfferResources1","OfferResources1","OfferResources1 method [DXGI]","OfferResources1 method [DXGI]","IDXGIDevice4 interface","direct3ddxgi.idxgidevice4_offerresources1","dxgi1_5/IDXGIDevice4::OfferResources1"]
old-location: direct3ddxgi\idxgidevice4_offerresources1.htm
tech.root: direct3ddxgi
ms.assetid: 7F6782F3-7779-4DBD-AD5A-AE0FB136FC70
ms.date: 12/05/2018
ms.keywords: IDXGIDevice4 interface [DXGI],OfferResources1 method, IDXGIDevice4.OfferResources1, IDXGIDevice4::OfferResources1, OfferResources1, OfferResources1 method [DXGI], OfferResources1 method [DXGI],IDXGIDevice4 interface, direct3ddxgi.idxgidevice4_offerresources1, dxgi1_5/IDXGIDevice4::OfferResources1
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDevice4::OfferResources1
 - dxgi1_5/IDXGIDevice4::OfferResources1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIDevice4.OfferResources1
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

An array of pointers to <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interfaces for the resources to offer.

### -param Priority [in]

Type: <b>DXGI_OFFER_RESOURCE_PRIORITY</b>

A <a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority">DXGI_OFFER_RESOURCE_PRIORITY</a>-typed value that indicates how valuable data is.

### -param Flags [in]

Type: <b>UINT</b>

Specifies the <a href="/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags">DXGI_OFFER_RESOURCE_FLAGS</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if a resource in the array, or the priority, is invalid.

## -remarks

<b>OfferResources1</b> (an extension of the original <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> API) enables D3D based applications to allow de-committing of an allocation’s backing store to reduce system commit under low memory conditions. 
A de-committed allocation cannot be reused, so opting in to the new DXGI_OFFER_RESOURCE_FLAG_ALLOW_DECOMMIT flag means the new reclaim results must be properly handled. Refer to the flag descriptions in <a href="/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results">DXGI_RECLAIM_RESOURCE_RESULTS</a> and the Example below.

<b>OfferResources1</b> and <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1">ReclaimResources1</a> may <i>not</i> be used interchangeably with <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">OfferResources</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">ReclaimResources</a>. 


The priority value that the  <i>Priority</i> parameter specifies describes how valuable the caller considers the content to be.  The operating system uses the priority value to discard resources in order of priority. The operating system discards a resource that is offered with low priority before it discards a resource that is  offered with a higher priority.

If you call <b>OfferResources1</b> to offer a resource while the resource is bound to the pipeline, the resource is unbound.  You cannot call <b>OfferResources1</b> on a resource that is mapped.  After you offer a resource, the resource cannot be mapped or bound to the pipeline until you call the <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1">ReclaimResources1</a> method to reclaim the resource. You cannot call <b>OfferResources1</b> to offer immutable resources.

To offer shared resources, call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">OfferResources1</a> on only one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a> object and then call <b>OfferResources1</b> only while you hold the mutex. In fact, you can't offer shared resources unless you use <b>IDXGIKeyedMutex</b> because offering shared resources without using <b>IDXGIKeyedMutex</b> isn't supported.

The user mode display driver might not immediately offer the resources that you specified in a call to <b>OfferResources1</b>. The driver can postpone offering them until the next call to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>, or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a>.


#### Examples

A UWP based application is being suspended to the background and wishes to offer its graphics resources back to the system, in case another application wants them. The application will reclaim these resources when it gets resumed. The application also realizes that the total available system commit is small on this platform, and is willing to allow its resources to be removed from the system commit. If the reclaim process fails because the system is out of memory, the application handles the error condition.  



``` syntax
struct Texture 
{ 
    UINT32 Width; 
    UINT32 Height; 
    UINT32 Mips; 
    ID3D11Texture2D* pResource; 
};  

void Application::OfferInterfaceResources(ID3D11Device* pD3D11Device) 
{ 
    CComPtr<IDXGIDevice4> pDXGIDevice; 
    ThrowIfFailed(pD3D11Device->QueryInterface(&pDXGIDevice)); 

    for(Texture& t : m_Textures) 
    { 
        CComPtr<IDXGIResource> pDXGIResource; 
        ThrowIfFailed(t.pResource->QueryInterface(&pDXGIResource));   
        ThrowIfFailed(pDXGIDevice->OfferResources1(1, &pDXGIResource, DXGI_OFFER_RESOURCE_PRIORITY_NORMAL, 
											DXGI_OFFER_RESOURCE_FLAG_ALLOW_DECOMMIT)); 
    } 
} 

void Application::ReclaimInterfaceResources (ID3D11Device* pD3D11Device) 
{ 
    CComPtr<IDXGIDevice4> pDXGIDevice; 
    ThrowIfFailed(pD3D11Device->QueryInterface(&pDXGIDevice));  

    for(Texture& t : m_Textures) 
    { 
        CComPtr<IDXGIResource> pDXGIResource; 
        ThrowIfFailed(t.pResource->QueryInterface(&pDXGIResource));       

        DXGI_RECLAIM_RESOURCE_RESULTS Result; 
        ThrowIfFailed(pDXGIDevice->ReclaimResources1(1, &pDXGIResource, &Result)); 

        // If the surface lost its backing commitment, it must be recreated. 

        if(Result == DXGI_RECLAIM_RESOURCE_RESULT_NOT_COMMITTED) 
        { 
            t.pResource->Release(); 
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

```


## -see-also

<a href="/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results">DXGI_RECLAIM_RESOURCE_RESULTS</a>



<a href="/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgidevice4">IDXGIDevice4</a>
