---
UID: NN:strmif.IEnumRegFilters
title: IEnumRegFilters (strmif.h)
description: Note  This interface has been deprecated.
old-location: dshow\ienumregfilters.htm
tech.root: DirectShow
ms.assetid: 59cb809d-84f5-42c4-a385-0f586af4d048
ms.date: 12/05/2018
ms.keywords: IEnumRegFilters, IEnumRegFilters interface [DirectShow], IEnumRegFilters interface [DirectShow],described, IEnumRegFiltersInterface, dshow.ienumregfilters, strmif/IEnumRegFilters
f1_keywords:
- strmif/IEnumRegFilters
dev_langs:
- c++
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
- IEnumRegFilters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumRegFilters interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper2-enummatchingfilters">IFilterMapper2::EnumMatchingFilters</a>, which enumerates monikers and returns a pointer to the <b>IEnumMoniker</b> interface.</div>
<div> </div>
This interface provides methods for enumerating registered filters. The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifiltermapper-enummatchingfilters">IFilterMapper::EnumMatchingFilters</a> method returns a pointer to this interface. However, <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper</a> has been deprecated in favor of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumRegFilters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumRegFilters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumRegFilters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumregfilters-clone">Clone</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumregfilters-next">Next</a>
</td>
<td align="left" width="63%">
Fills an array with the next filters that meet the requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumregfilters-reset">Reset</a>
</td>
<td align="left" width="63%">
Makes the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumregfilters-next">Next</a> method start again, beginning at the first filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumregfilters-skip">Skip</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

