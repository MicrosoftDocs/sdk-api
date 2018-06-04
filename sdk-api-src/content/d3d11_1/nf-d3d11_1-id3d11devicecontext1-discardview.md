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

# ID3D11DeviceContext1::DiscardView


## -description


Discards a resource view from the device context.


## -parameters




### -param pResourceView [in]

Type: <b><a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a> interface for the resource view to discard. The resource that underlies the view must have been created with usage <a href="d3d11_usage.htm">D3D11_USAGE_DEFAULT</a> or <a href="d3d11_usage.htm">D3D11_USAGE_DYNAMIC</a>, otherwise the runtime drops the call to <b>DiscardView</b>; if the debug layer is enabled, the runtime returns an error message.


## -returns



Returns nothing




## -remarks



<b>DiscardView</b> informs the graphics processing unit (GPU) that the existing content in the resource view that <i>pResourceView</i> points to is no longer needed.  The view can be an SRV, RTV, UAV, or DSV.  <b>DiscardView</b> is a variation on the <a href="https://msdn.microsoft.com/6C27231E-BF61-4D50-B5B1-59961B82534B">DiscardResource</a> method.  <b>DiscardView</b> allows you to discard a subset of a resource that is in a view (such as a single miplevel).  More importantly, <b>DiscardView</b> provides a convenience because often views are what are being bound and unbound at the pipeline.  Some pipeline bindings do not have views, such as stream output.  In that situation, <b>DiscardResource</b> can do the job for any resource.




## -see-also




<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

