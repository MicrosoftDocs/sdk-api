---
UID: NN:strmif.IBaseFilter
title: IBaseFilter (strmif.h)
description: The IBaseFilter interface is the primary interface for DirectShow filters.
helpviewer_keywords: ["IBaseFilter","IBaseFilter interface [DirectShow]","IBaseFilter interface [DirectShow]","described","IBaseFilterInterface","dshow.ibasefilter","strmif/IBaseFilter"]
old-location: dshow\ibasefilter.htm
tech.root: DirectShow
ms.assetid: d8c09dc7-dae8-4b51-8da8-69e64928a091
ms.date: 12/05/2018
ms.keywords: IBaseFilter, IBaseFilter interface [DirectShow], IBaseFilter interface [DirectShow],described, IBaseFilterInterface, dshow.ibasefilter, strmif/IBaseFilter
f1_keywords:
- strmif/IBaseFilter
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBaseFilter interface


## -description



The <code>IBaseFilter</code> interface is the primary interface for DirectShow filters. All DirectShow filters must expose this interface. The Filter Graph Manager uses this interface to control filters. Applications can use this interface to enumerate pins and query for filter information, but should not use it to change the state of a filter. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a> interface on the Filter Graph Manager.

<b>Filter developers</b>: Implement this interface on every DirectShow filter. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cbasefilter">CBaseFilter</a> base class implements this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBaseFilter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter</a>. <b>IBaseFilter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-enumpins">EnumPins</a>
</td>
<td align="left" width="63%">
Enumerates the pins on this filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-findpin">FindPin</a>
</td>
<td align="left" width="63%">
Retrieves the pin with the specified identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-joinfiltergraph">JoinFilterGraph</a>
</td>
<td align="left" width="63%">
Notifies the filter that it has joined or left the filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-queryfilterinfo">QueryFilterInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-queryvendorinfo">QueryVendorInfo</a>
</td>
<td align="left" width="63%">
Retrieves a string containing vendor information.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter</a>
 

 

