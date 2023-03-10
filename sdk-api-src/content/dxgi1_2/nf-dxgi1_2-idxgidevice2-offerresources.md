---
UID: NF:dxgi1_2.IDXGIDevice2.OfferResources
title: IDXGIDevice2::OfferResources (dxgi1_2.h)
description: Allows the operating system to free the video memory of resources by discarding their content. (IDXGIDevice2.OfferResources)
helpviewer_keywords: ["IDXGIDevice2 interface [DXGI]","OfferResources method","IDXGIDevice2.OfferResources","IDXGIDevice2::OfferResources","OfferResources","OfferResources method [DXGI]","OfferResources method [DXGI]","IDXGIDevice2 interface","direct3ddxgi.idxgidevice2_offerresources","dxgi1_2/IDXGIDevice2::OfferResources"]
old-location: direct3ddxgi\idxgidevice2_offerresources.htm
tech.root: direct3ddxgi
ms.assetid: E642DDD5-17FE-4BB9-823F-1DA51C281253
ms.date: 12/05/2018
ms.keywords: IDXGIDevice2 interface [DXGI],OfferResources method, IDXGIDevice2.OfferResources, IDXGIDevice2::OfferResources, OfferResources, OfferResources method [DXGI], OfferResources method [DXGI],IDXGIDevice2 interface, direct3ddxgi.idxgidevice2_offerresources, dxgi1_2/IDXGIDevice2::OfferResources
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDevice2::OfferResources
 - dxgi1_2/IDXGIDevice2::OfferResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDevice2.OfferResources
---

# IDXGIDevice2::OfferResources


## -description

Allows the operating system to free the video memory of resources by discarding their content.

## -parameters

### -param NumResources [in]

The number of resources in the <i>ppResources</i> argument array.

### -param ppResources [in]

An array of pointers to <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interfaces for the resources to offer.

### -param Priority [in]

A <a href="/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority">DXGI_OFFER_RESOURCE_PRIORITY</a>-typed value that indicates how valuable data is.

## -returns

<b>OfferResources</b> returns:
            
          

<ul>
<li>S_OK if resources were successfully offered</li>
<li>E_INVALIDARG if a resource in the array or the priority is invalid</li>
</ul>

## -remarks

The priority value that the  <i>Priority</i> parameter specifies describes how valuable the caller considers the content to be.  The operating system uses the priority value to discard resources in order of priority. The operating system discards a resource that is offered with low priority before it discards a resource that is  offered with a higher priority.

If you call <b>OfferResources</b> to offer a resource while the resource is bound to the pipeline, the resource is unbound.  You cannot call <b>OfferResources</b> on a resource that is mapped.  After you offer a resource, the resource cannot be mapped or bound to the pipeline until you call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">IDXGIDevice2::ReclaimResource</a> method to reclaim the resource. You cannot call <b>OfferResources</b> to offer immutable resources.

To offer shared resources, call <b>OfferResources</b> on only one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a> object and then call <b>OfferResources</b> only while you hold the mutex. In fact, you can't offer shared resources unless you use <b>IDXGIKeyedMutex</b> because offering shared resources without using <b>IDXGIKeyedMutex</b> isn't supported.

<div class="alert"><b>Note</b>  The user mode display driver might not immediately offer the resources that you specified in a call to <b>OfferResources</b>. The driver can postpone offering them until the next call to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a>, or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a>. </div>
<div> </div>
<b>Platform Update for Windows 7:  </b>The runtime validates that <b>OfferResources</b> is used correctly on non-shared resources but doesn't perform the intended functionality. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">IDXGIDevice2::ReclaimResource</a>
