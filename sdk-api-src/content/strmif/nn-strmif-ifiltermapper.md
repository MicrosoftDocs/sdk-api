---
UID: NN:strmif.IFilterMapper
title: IFilterMapper (strmif.h)
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\ifiltermapper.htm
tech.root: DirectShow
ms.assetid: e2f32235-e331-4c3c-925a-7cfa531e9ab3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFilterMapper, IFilterMapper interface [DirectShow], IFilterMapper interface [DirectShow],described, IFilterMapperInterface, dshow.ifiltermapper, strmif/IFilterMapper
ms.topic: interface
f1_keywords: 
 - "strmif/IFilterMapper"
req.header: strmif.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IFilterMapper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFilterMapper interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. It will continue to be supported for backward compatibility with existing applications, but new applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> interface.</div>
<div> </div>
This interface provides methods for registering and unregistering filters, and for looking up filters based on their characteristics.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilterMapper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFilterMapper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilterMapper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-enummatchingfilters">EnumMatchingFilters</a>
</td>
<td align="left" width="63%">
Finds all filters matching specific requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-registerfilter">RegisterFilter</a>
</td>
<td align="left" width="63%">
Records the details of a filter in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-registerfilterinstance">RegisterFilterInstance</a>
</td>
<td align="left" width="63%">
Registers an identifiable instance of a filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-registerpin">RegisterPin</a>
</td>
<td align="left" width="63%">
Records the details of a pin in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-registerpintype">RegisterPinType</a>
</td>
<td align="left" width="63%">
Adds a type for the pin to the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-unregisterfilter">UnregisterFilter</a>
</td>
<td align="left" width="63%">
Deletes a filter from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-unregisterfilterinstance">UnregisterFilterInstance</a>
</td>
<td align="left" width="63%">
Deletes an identifiable instance of a filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-unregisterpin">UnregisterPin</a>
</td>
<td align="left" width="63%">
Deletes a pin from the registry.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

