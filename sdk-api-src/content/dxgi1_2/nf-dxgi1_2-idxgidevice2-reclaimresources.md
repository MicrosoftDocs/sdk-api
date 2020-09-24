---
UID: NF:dxgi1_2.IDXGIDevice2.ReclaimResources
title: IDXGIDevice2::ReclaimResources (dxgi1_2.h)
description: Restores access to resources that were previously offered by calling IDXGIDevice2::OfferResources.
helpviewer_keywords: ["IDXGIDevice2 interface [DXGI]","ReclaimResources method","IDXGIDevice2.ReclaimResources","IDXGIDevice2::ReclaimResources","ReclaimResources","ReclaimResources method [DXGI]","ReclaimResources method [DXGI]","IDXGIDevice2 interface","direct3ddxgi.idxgidevice2_reclaimresources","dxgi1_2/IDXGIDevice2::ReclaimResources"]
old-location: direct3ddxgi\idxgidevice2_reclaimresources.htm
tech.root: direct3ddxgi
ms.assetid: 30533605-0F5A-4D15-B01E-7C23E2AE775E
ms.date: 12/05/2018
ms.keywords: IDXGIDevice2 interface [DXGI],ReclaimResources method, IDXGIDevice2.ReclaimResources, IDXGIDevice2::ReclaimResources, ReclaimResources, ReclaimResources method [DXGI], ReclaimResources method [DXGI],IDXGIDevice2 interface, direct3ddxgi.idxgidevice2_reclaimresources, dxgi1_2/IDXGIDevice2::ReclaimResources
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
 - IDXGIDevice2::ReclaimResources
 - dxgi1_2/IDXGIDevice2::ReclaimResources
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
 - IDXGIDevice2.ReclaimResources
---

# IDXGIDevice2::ReclaimResources


## -description

Restores access to resources that were previously offered by calling <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a>.

## -parameters

### -param NumResources [in]

The number of resources in the <i>ppResources</i> argument and <i>pDiscarded</i> argument arrays.

### -param ppResources [in]

An array of pointers to <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interfaces for the resources to reclaim.

### -param pDiscarded [out, optional]

A pointer to an array that receives Boolean values. Each value in the array corresponds to a resource at the same index that the <i>ppResources</i> parameter specifies.  The runtime sets each Boolean value to TRUE if the corresponding resource’s content was discarded and is now undefined, or to FALSE if the corresponding resource’s old content is still intact.  The caller can pass in <b>NULL</b>, if the caller intends to fill the resources with new content regardless of whether the old content was discarded.

## -returns

<b>ReclaimResources</b> returns:
            
          

<ul>
<li>S_OK if resources were successfully reclaimed</li>
<li>E_INVALIDARG if the resources are invalid</li>
</ul>

## -remarks

After you call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> to offer one or more resources, you must call <b>ReclaimResources</b> before you can use those resources again.  You must check the values in the array at <i>pDiscarded</i> to determine whether each resource’s content was discarded. If a resource’s content was discarded while it was offered, its current content is undefined. Therefore, you must overwrite the resource’s content before you use the resource.

To reclaim shared resources, call <b>ReclaimResources</b> only on one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a> object and then call <b>ReclaimResources</b> only while you hold the mutex.

<b>Platform Update for Windows 7:  </b>The runtime validates that <b>ReclaimResources</b> is used correctly on non-shared resources but doesn't perform the intended functionality. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a>