---
UID: NN:strmif.IBaseFilter
title: IBaseFilter
author: windows-sdk-content
description: The IBaseFilter interface is the primary interface for DirectShow filters.
old-location: dshow\ibasefilter.htm
old-project: DirectShow
ms.assetid: d8c09dc7-dae8-4b51-8da8-69e64928a091
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IBaseFilter, IBaseFilter interface [DirectShow], IBaseFilter interface [DirectShow],described, IBaseFilterInterface, dshow.ibasefilter, strmif/IBaseFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBaseFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IBaseFilter interface


## -description



The <code>IBaseFilter</code> interface is the primary interface for DirectShow filters. All DirectShow filters must expose this interface. The Filter Graph Manager uses this interface to control filters. Applications can use this interface to enumerate pins and query for filter information, but should not use it to change the state of a filter. Instead, use the <a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl</a> interface on the Filter Graph Manager.

<b>Filter developers</b>: Implement this interface on every DirectShow filter. The <a href="https://msdn.microsoft.com/4610c8d6-9d7d-47ca-b1d5-0a867153a5f6">CBaseFilter</a> base class implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBaseFilter</b> interface inherits from <a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter</a>. <b>IBaseFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBaseFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02675c93-7901-40f6-a9fc-f6f13f56acca">EnumPins</a>
</td>
<td align="left" width="63%">
Enumerates the pins on this filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bdefaeb-f631-4b79-9965-c1c570e0ff80">FindPin</a>
</td>
<td align="left" width="63%">
Retrieves the pin with the specified identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f01c71f-5c12-4bf3-937c-740168baf776">JoinFilterGraph</a>
</td>
<td align="left" width="63%">
Notifies the filter that it has joined or left the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cb9b6ef-05ae-4816-b337-dd90cab843fb">QueryFilterInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7524de26-360e-49c7-b636-7d05cf4d0ad2">QueryVendorInfo</a>
</td>
<td align="left" width="63%">
Retrieves a string containing vendor information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5c0060e8-a9e5-4141-a38d-9a1bc55cc91b">IMediaFilter</a>
 

 

