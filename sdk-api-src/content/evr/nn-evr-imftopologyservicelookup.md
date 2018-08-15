---
UID: NN:evr.IMFTopologyServiceLookup
title: IMFTopologyServiceLookup
author: windows-sdk-content
description: Enables a custom video mixer or video presenter to get interface pointers from the Enhanced Video Renderer (EVR).
old-location: mf\imftopologyservicelookup.htm
old-project: medfound
ms.assetid: a912c17a-40ef-441c-bfc9-7ef49d22070f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFTopologyServiceLookup, IMFTopologyServiceLookup interface [Media Foundation], IMFTopologyServiceLookup interface [Media Foundation],described, a912c17a-40ef-441c-bfc9-7ef49d22070f, evr/IMFTopologyServiceLookup, mf.imftopologyservicelookup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTopologyServiceLookup
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFTopologyServiceLookup interface


## -description


Enables a custom video mixer or video presenter to get interface pointers from the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR). The mixer can also use this interface to get interface pointers from the presenter, and the presenter can use it to get interface pointers from the mixer.

To use this interface, implement the <a href="https://msdn.microsoft.com/c4215d08-3734-44b9-b053-0d49d89a90f6">IMFTopologyServiceLookupClient</a> interface on your custom mixer or presenter. The EVR calls <a href="https://msdn.microsoft.com/b89f5a47-154c-455a-b5a2-db55e4972b21">IMFTopologyServiceLookupClient::InitServicePointers</a> with a pointer to the EVR's <b>IMFTopologyServiceLookup</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopologyServiceLookup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTopologyServiceLookup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopologyServiceLookup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba0dbfdf-1bab-42ba-910f-04a3f37be955">LookupService</a>
</td>
<td align="left" width="63%">
Retrieves an interface from the EVR, or from the video mixer or video presenter.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

