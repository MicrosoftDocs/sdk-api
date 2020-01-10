---
UID: NN:mpeg2data.ISectionList
title: ISectionList (mpeg2data.h)
description: The ISectionList interface represents a list of MPEG-2 table sections.
old-location: mstv\isectionlist.htm
tech.root: mstv
ms.assetid: eb6d31b4-ee4a-468f-9e58-115159095858
ms.date: 12/05/2018
ms.keywords: ISectionList, ISectionList interface [Microsoft TV Technologies], ISectionList interface [Microsoft TV Technologies],described, ISectionListInterface, mpeg2data/ISectionList, mstv.isectionlist
f1_keywords:
- mpeg2data/ISectionList
dev_langs:
- c++
req.header: mpeg2data.h
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
- Mpeg2data.h
api_name:
- ISectionList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISectionList interface


## -description



The <b>ISectionList</b> interface represents a list of MPEG-2 table sections.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISectionList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISectionList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISectionList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-cancelpendingrequest">CancelPendingRequest</a>
</td>
<td align="left" width="63%">
Cancels any pending asynchronous request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-getnumberofsections">GetNumberOfSections</a>
</td>
<td align="left" width="63%">
Returns the number of MPEG-2 sections that were received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-getprogramidentifier">GetProgramIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the program identifier (PID) of the packets that this object is receiving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-getsectiondata">GetSectionData</a>
</td>
<td align="left" width="63%">
Retrieves a section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-gettableidentifier">GetTableIdentifier</a>
</td>
<td align="left" width="63%">
Returns the table identifier (TID) of the packets that this object is receiving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-isectionlist-initializewithrawsections">InitializeWithRawSections</a>
</td>
<td align="left" width="63%">
Initializes the object with raw section data.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISectionList)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

