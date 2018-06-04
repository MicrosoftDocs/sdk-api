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

# IDXGIDevice4::ReclaimResources1


## -description


Restores access to resources that were previously offered by calling <a href="https://msdn.microsoft.com/7F6782F3-7779-4DBD-AD5A-AE0FB136FC70">IDXGIDevice4::OfferResources1</a>.


## -parameters




### -param NumResources [in]

Type: <b>UINT</b>

The number of resources in the <i>ppResources</i> argument and <i>pResults</i> argument arrays.


### -param ppResources [in]

Type: <b>IDXGIResource*</b>

An array of pointers to <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> interfaces for the resources to reclaim.


### -param pResults [out]

Type: <b><a href="https://msdn.microsoft.com/AF7082A5-6280-4602-9944-EC2DFF91BBB9">DXGI_RECLAIM_RESOURCE_RESULTS</a>*</b>

A pointer to an array that receives <a href="https://msdn.microsoft.com/AF7082A5-6280-4602-9944-EC2DFF91BBB9">DXGI_RECLAIM_RESOURCE_RESULTS</a> values. Each value in the array corresponds to a resource at the same index that the <i>ppResources</i> parameter specifies.  The caller can pass in <b>NULL</b>, if the caller intends to fill the resources with new content regardless of whether the old content was discarded.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code, including E_INVALIDARG if the resources are invalid.




## -remarks



After you call <a href="https://msdn.microsoft.com/7F6782F3-7779-4DBD-AD5A-AE0FB136FC70">OfferResources1</a> to offer one or more resources, you must call <b>ReclaimResources1</b> before you can use those resources again.

To reclaim shared resources, call <b>ReclaimResources1</b> only on one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a> object and then call <b>ReclaimResources1</b> only while you hold the mutex.




## -see-also




<a href="https://msdn.microsoft.com/15EA6B68-587E-4D92-A70D-7DDA9915EBC2">IDXGIDevice4</a>



<a href="https://msdn.microsoft.com/30533605-0F5A-4D15-B01E-7C23E2AE775E">ReclaimResources</a>
 

 

