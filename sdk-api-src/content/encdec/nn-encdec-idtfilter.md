---
UID: NN:encdec.IDTFilter
title: IDTFilter (encdec.h)
author: windows-sdk-content
description: The IDTFilter interface is exposed by the Decrypter/Detagger filter. Applications can use this interface to set the ratings permissions.
old-location: mstv\idtfilter.htm
tech.root: mstv
ms.assetid: 15acf764-7e4d-40c3-b907-ff5dfaa69dae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDTFilter, IDTFilter interface [Microsoft TV Technologies], IDTFilter interface [Microsoft TV Technologies],described, IDTFilterInterface, encdec/IDTFilter, mstv.idtfilter
ms.topic: interface
f1_keywords: 
 - "encdec/IDTFilter"
dev_langs:
 - c++
req.header: encdec.h
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
 - EncDec.h
api_name:
 - IDTFilter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilter interface


## -description



The <b>IDTFilter</b> interface is exposed by the Decrypter/Detagger filter. Applications can use this interface to set the ratings permissions.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDTFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDTFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-get_blockedratingattributes">get_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Determines whether content is blocked for a given rating system and rating level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-get_blockunrated">get_BlockUnRated</a>
</td>
<td align="left" width="63%">
Indicates whether a program without rating information is blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-get_blockunrateddelay">get_BlockUnRatedDelay</a>
</td>
<td align="left" width="63%">
Retrieves that length of time the filter waits before it blocks unrated content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-get_evalratobjok">get_EvalRatObjOK</a>
</td>
<td align="left" width="63%">
Queries whether the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/evalrat-object">EvalRat</a> object was created successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-getcurrrating">GetCurrRating</a>
</td>
<td align="left" width="63%">
Retrieves the current rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-put_blockedratingattributes">put_BlockedRatingAttributes</a>
</td>
<td align="left" width="63%">
Specifies whether to block content that has a specified rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-put_blockunrated">put_BlockUnRated</a>
</td>
<td align="left" width="63%">
Specifies whether to block a program for which rating information has not been obtained.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter-put_blockunrateddelay">put_BlockUnRatedDelay</a>
</td>
<td align="left" width="63%">
Sets the length of time the filter waits before it blocks unrated content.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilter)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

