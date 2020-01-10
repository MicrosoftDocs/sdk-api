---
UID: NN:tvratings.IXDSToRat
title: IXDSToRat (tvratings.h)
description: The IXDSToRat interface parses rating information from extended data services (XDS) information in line 21.
old-location: mstv\ixdstorat.htm
tech.root: mstv
ms.assetid: de65e5cd-3f4b-4925-a6b8-636fc2e332ec
ms.date: 12/05/2018
ms.keywords: IXDSToRat, IXDSToRat interface [Microsoft TV Technologies], IXDSToRat interface [Microsoft TV Technologies],described, IXDSToRatInterface, mstv.ixdstorat, tvratings/IXDSToRat
f1_keywords:
- tvratings/IXDSToRat
dev_langs:
- c++
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
- Tvratings.h
api_name:
- IXDSToRat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXDSToRat interface


## -description



The <b>IXDSToRat</b> interface parses rating information from extended data services (XDS) information in line 21. This interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> (ratings decoder) object. The XDSToRat object is implemented by third parties.

The XDS Codec filter uses this interface. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXDSToRat</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IXDSToRat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXDSToRat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ixdstorat-init">Init</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object to its initial state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ixdstorat-parsexdsbytepair">ParseXDSBytePair</a>
</td>
<td align="left" width="63%">
Parses a single byte pair from an XDS stream.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IXDSToRat)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

