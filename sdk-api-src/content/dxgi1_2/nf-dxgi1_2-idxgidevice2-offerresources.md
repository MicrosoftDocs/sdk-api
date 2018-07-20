---
UID: NF:dxgi1_2.IDXGIDevice2.OfferResources
title: IDXGIDevice2::OfferResources
author: windows-sdk-content
description: Allows the operating system to free the video memory of resources by discarding their content.
old-location: direct3ddxgi\idxgidevice2_offerresources.htm
old-project: direct3ddxgi
ms.assetid: E642DDD5-17FE-4BB9-823F-1DA51C281253
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IDXGIDevice2 interface [DXGI],OfferResources method, IDXGIDevice2.OfferResources, IDXGIDevice2::OfferResources, OfferResources, OfferResources method [DXGI], OfferResources method [DXGI],IDXGIDevice2 interface, direct3ddxgi.idxgidevice2_offerresources, dxgi1_2/IDXGIDevice2::OfferResources
ms.prod: windows
ms.technology: windows-sdk
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
 - IDXGIDevice2.OfferResources
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice2::OfferResources


## -description


Allows the operating system to free the video memory of resources by discarding their content.


## -parameters




### -param NumResources [in]

The number of resources in the <i>ppResources</i> argument array.


### -param ppResources [in]

An array of pointers to <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> interfaces for the resources to offer.


### -param Priority [in]

A <a href="https://msdn.microsoft.com/BDC0AAA3-2B72-4732-82CE-458C14B0D993">DXGI_OFFER_RESOURCE_PRIORITY</a>-typed value that indicates how valuable data is.


## -returns



<b>OfferResources</b> returns:
            
          

<ul>
<li>S_OK if resources were successfully offered</li>
<li>E_INVALIDARG if a resource in the array or the priority is invalid</li>
</ul>



## -remarks



The priority value that the  <i>Priority</i> parameter specifies describes how valuable the caller considers the content to be.  The operating system uses the priority value to discard resources in order of priority. The operating system discards a resource that is offered with low priority before it discards a resource that is  offered with a higher priority.

If you call <b>OfferResources</b> to offer a resource while the resource is bound to the pipeline, the resource is unbound.  You cannot call <b>OfferResources</b> on a resource that is mapped.  After you offer a resource, the resource cannot be mapped or bound to the pipeline until you call the <a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">IDXGIDevice2::ReclaimResource</a> method to reclaim the resource. You cannot call <b>OfferResources</b> to offer immutable resources.

To offer shared resources, call <b>OfferResources</b> on only one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a> object and then call <b>OfferResources</b> only while you hold the mutex. In fact, you can't offer shared resources unless you use <b>IDXGIKeyedMutex</b> because offering shared resources without using <b>IDXGIKeyedMutex</b> isn't supported.

<div class="alert"><b>Note</b>  The user mode display driver might not immediately offer the resources that you specified in a call to <b>OfferResources</b>. The driver can postpone offering them until the next call to <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>, <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a>, or <a href="https://msdn.microsoft.com/e204c585-4996-4274-a654-b9912e957fe6">ID3D11DeviceContext::Flush</a>. </div>
<div> </div>
<b>Platform Update for Windows 7:  </b>The runtime validates that <b>OfferResources</b> is used correctly on non-shared resources but doesn't perform the intended functionality. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>



<a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">IDXGIDevice2::ReclaimResource</a>
 

 

