---
UID: NF:dxgi1_5.IDXGIDevice4.ReclaimResources1
title: IDXGIDevice4::ReclaimResources1 (dxgi1_5.h)
author: windows-sdk-content
description: Restores access to resources that were previously offered by calling IDXGIDevice4::OfferResources1.
old-location: direct3ddxgi\idxgidevice4_reclaimresources1.htm
tech.root: direct3ddxgi
ms.assetid: 83D09C41-CB96-4ADA-AE38-7D9542CCCFE0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIDevice4 interface [DXGI],ReclaimResources1 method, IDXGIDevice4.ReclaimResources1, IDXGIDevice4::ReclaimResources1, ReclaimResources1, ReclaimResources1 method [DXGI], ReclaimResources1 method [DXGI],IDXGIDevice4 interface, direct3ddxgi.idxgidevice4_reclaimresources1, dxgi1_5/IDXGIDevice4::ReclaimResources1
ms.topic: method
f1_keywords:
- dxgi1_5/IDXGIDevice4.ReclaimResources1
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dxgi.dll
api_name:
- IDXGIDevice4.ReclaimResources1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDevice4::ReclaimResources1


## -description


Restores access to resources that were previously offered by calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1">IDXGIDevice4::OfferResources1</a>.


## -parameters




### -param NumResources [in]

Type: <b>UINT</b>

The number of resources in the <i>ppResources</i> argument and <i>pResults</i> argument arrays.


### -param ppResources [in]

Type: <b>IDXGIResource*</b>

An array of pointers to <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interfaces for the resources to reclaim.


### -param pResults [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results">DXGI_RECLAIM_RESOURCE_RESULTS</a>*</b>

A pointer to an array that receives <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results">DXGI_RECLAIM_RESOURCE_RESULTS</a> values. Each value in the array corresponds to a resource at the same index that the <i>ppResources</i> parameter specifies.  The caller can pass in <b>NULL</b>, if the caller intends to fill the resources with new content regardless of whether the old content was discarded.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code, including E_INVALIDARG if the resources are invalid.




## -remarks



After you call <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1">OfferResources1</a> to offer one or more resources, you must call <b>ReclaimResources1</b> before you can use those resources again.

To reclaim shared resources, call <b>ReclaimResources1</b> only on one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex">IDXGIKeyedMutex</a> object and then call <b>ReclaimResources1</b> only while you hold the mutex.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgidevice4">IDXGIDevice4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">ReclaimResources</a>
 

 

