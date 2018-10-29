---
UID: NN:evr.IMFTopologyServiceLookupClient
title: IMFTopologyServiceLookupClient
author: windows-sdk-content
description: Initializes a video mixer or presenter.
old-location: mf\imftopologyservicelookupclient.htm
tech.root: medfound
ms.assetid: c4215d08-3734-44b9-b053-0d49d89a90f6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFTopologyServiceLookupClient, IMFTopologyServiceLookupClient interface [Media Foundation], IMFTopologyServiceLookupClient interface [Media Foundation],described, c4215d08-3734-44b9-b053-0d49d89a90f6, evr/IMFTopologyServiceLookupClient, mf.imftopologyservicelookupclient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTopologyServiceLookupClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTopologyServiceLookupClient interface


## -description


Initializes a video mixer or presenter. This interface is implemented by mixers and presenters, and enables them to query the enhanced video renderer (EVR) for interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopologyServiceLookupClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTopologyServiceLookupClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopologyServiceLookupClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b89f5a47-154c-455a-b5a2-db55e4972b21">InitServicePointers</a>
</td>
<td align="left" width="63%">
Signals the mixer or presenter to query the EVR for interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03ed29b4-89c1-4702-a23f-d013eeef5d44">ReleaseServicePointers</a>
</td>
<td align="left" width="63%">
Signals the mixer or presenter to release the interface pointers obtained from the EVR.

</td>
</tr>
</table> 


## -remarks



When the EVR loads the video mixer and the video presenter, the EVR queries the object for this interface and calls <a href="https://msdn.microsoft.com/b89f5a47-154c-455a-b5a2-db55e4972b21">InitServicePointers</a>. Inside the <b>InitServicePointers</b> method, the object can query the EVR for interface pointers.




## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/a912c17a-40ef-441c-bfc9-7ef49d22070f">IMFTopologyServiceLookup</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

