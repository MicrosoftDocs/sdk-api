---
UID: NF:dxgi1_2.IDXGIDevice2.ReclaimResources
title: IDXGIDevice2::ReclaimResources (dxgi1_2.h)
author: windows-sdk-content
description: Restores access to resources that were previously offered by calling IDXGIDevice2::OfferResources.
old-location: direct3ddxgi\idxgidevice2_reclaimresources.htm
tech.root: direct3ddxgi
ms.assetid: 30533605-0F5A-4D15-B01E-7C23E2AE775E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIDevice2 interface [DXGI],ReclaimResources method, IDXGIDevice2.ReclaimResources, IDXGIDevice2::ReclaimResources, ReclaimResources, ReclaimResources method [DXGI], ReclaimResources method [DXGI],IDXGIDevice2 interface, direct3ddxgi.idxgidevice2_reclaimresources, dxgi1_2/IDXGIDevice2::ReclaimResources
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDevice2::ReclaimResources


## -description


Restores access to resources that were previously offered by calling <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a>.


## -parameters




### -param NumResources [in]

The number of resources in the <i>ppResources</i> argument and <i>pDiscarded</i> argument arrays.


### -param ppResources [in]

An array of pointers to <a href="https://msdn.microsoft.com/en-us/library/Bb174560(v=VS.85).aspx">IDXGIResource</a> interfaces for the resources to reclaim.


### -param pDiscarded [out, optional]

A pointer to an array that receives Boolean values. Each value in the array corresponds to a resource at the same index that the <i>ppResources</i> parameter specifies.  The runtime sets each Boolean value to TRUE if the corresponding resource’s content was discarded and is now undefined, or to FALSE if the corresponding resource’s old content is still intact.  The caller can pass in <b>NULL</b>, if the caller intends to fill the resources with new content regardless of whether the old content was discarded.


## -returns



<b>ReclaimResources</b> returns:
            
          

<ul>
<li>S_OK if resources were successfully reclaimed</li>
<li>E_INVALIDARG if the resources are invalid</li>
</ul>



## -remarks



After you call <a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a> to offer one or more resources, you must call <b>ReclaimResources</b> before you can use those resources again.  You must check the values in the array at <i>pDiscarded</i> to determine whether each resource’s content was discarded. If a resource’s content was discarded while it was offered, its current content is undefined. Therefore, you must overwrite the resource’s content before you use the resource.

To reclaim shared resources, call <b>ReclaimResources</b> only on one of the sharing devices.  To ensure exclusive access to the resources, you must use an <a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a> object and then call <b>ReclaimResources</b> only while you hold the mutex.

<b>Platform Update for Windows 7:  </b>The runtime validates that <b>ReclaimResources</b> is used correctly on non-shared resources but doesn't perform the intended functionality. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>



<a href="https://msdn.microsoft.com/E642DDD5-17FE-4BB9-823F-1DA51C281253">IDXGIDevice2::OfferResources</a>
 

 

