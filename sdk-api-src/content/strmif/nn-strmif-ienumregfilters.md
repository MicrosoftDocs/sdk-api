---
UID: NN:strmif.IEnumRegFilters
title: IEnumRegFilters
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\ienumregfilters.htm
tech.root: DirectShow
ms.assetid: 59cb809d-84f5-42c4-a385-0f586af4d048
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IEnumRegFilters, IEnumRegFilters interface [DirectShow], IEnumRegFilters interface [DirectShow],described, IEnumRegFiltersInterface, dshow.ienumregfilters, strmif/IEnumRegFilters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumRegFilters interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should call <a href="https://msdn.microsoft.com/f121b4c3-fce1-4be3-ace4-5084242130f6">IFilterMapper2::EnumMatchingFilters</a>, which enumerates monikers and returns a pointer to the <b>IEnumMoniker</b> interface.</div>
<div> </div>
This interface provides methods for enumerating registered filters. The <a href="https://msdn.microsoft.com/602a7568-f5f8-4705-a2bc-6b9408bbbe54">IFilterMapper::EnumMatchingFilters</a> method returns a pointer to this interface. However, <a href="https://msdn.microsoft.com/e2f32235-e331-4c3c-925a-7cfa531e9ab3">IFilterMapper</a> has been deprecated in favor of <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumRegFilters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumRegFilters</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ba4366fa-57ba-4057-b3b9-5380e0fca006">Clone</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec255b9b-33cf-42a3-9f02-f1f34eee2da1">Next</a>
</td>
<td align="left" width="63%">
Fills an array with the next filters that meet the requirements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/095d0102-c845-48ba-a1f5-e0262a924b50">Reset</a>
</td>
<td align="left" width="63%">
Makes the <a href="https://msdn.microsoft.com/ec255b9b-33cf-42a3-9f02-f1f34eee2da1">Next</a> method start again, beginning at the first filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d774ea12-cc06-47c5-82ee-c1ec761e0097">Skip</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

