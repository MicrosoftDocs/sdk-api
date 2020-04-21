---
UID: NN:tvratings.IEvalRat
title: IEvalRat (tvratings.h)
description: The IEvalRat interface is used to evaluate content ratings carried by a broadcast stream.helpviewer_keywords: ["IEvalRat","IEvalRat interface [Microsoft TV Technologies]","IEvalRat interface [Microsoft TV Technologies]","described","IEvalRatInterface","mstv.ievalrat","tvratings/IEvalRat"]
old-location: mstv\ievalrat.htm
tech.root: mstv
ms.assetid: b37c7e7d-80fd-4a42-a698-c20ffb2a5052
ms.date: 12/05/2018
ms.keywords: IEvalRat, IEvalRat interface [Microsoft TV Technologies], IEvalRat interface [Microsoft TV Technologies],described, IEvalRatInterface, mstv.ievalrat, tvratings/IEvalRat
f1_keywords:
- tvratings/IEvalRat
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
- IEvalRat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEvalRat interface


## -description



The <b>IEvalRat</b> interface is used to evaluate content ratings carried by a broadcast stream. This interface is exposed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/evalrat-object">EvalRat</a> (ratings evaluator) object. The EvalRat object is implemented by third parties.

The Encrypter/Tagger filter and the Decrypter/Detagger filter use this interface. Applications use the interfaces exposed by those filters, but typically do not use the <b>IEvalRat</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEvalRat</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IEvalRat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEvalRat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-get_blockedratingattributes">get_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Determines whether content is blocked for a given rating system and rating level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-get_blockunrated">get_BlockUnRated</a>
</td>
<td align="left" width="63%">
Indicates whether a program without rating information is blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-mostrestrictiverating">MostRestrictiveRating</a>
</td>
<td align="left" width="63%">
Compares two ratings and returns the more restrictive of the two.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-put_blockedratingattributes">put_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Specifies whether to block content that has a specified rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-put_blockunrated">put_BlockUnRated</a>
</td>
<td align="left" width="63%">
Specifies whether to block a program for which rating information has not been obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-testrating">TestRating</a>
</td>
<td align="left" width="63%">
Determines whether a program with the specified rating should be blocked.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEvalRat)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

