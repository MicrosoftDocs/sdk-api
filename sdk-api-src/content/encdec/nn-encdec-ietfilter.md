---
UID: NN:encdec.IETFilter
title: IETFilter (encdec.h)
description: The IETFilter interface is exposed by the Encrypter/Tagger filter. Most applications will not have to use this interface.
helpviewer_keywords: ["IETFilter","IETFilter interface [Microsoft TV Technologies]","IETFilter interface [Microsoft TV Technologies]","described","IETFilterInterface","encdec/IETFilter","mstv.ietfilter"]
old-location: mstv\ietfilter.htm
tech.root: mstv
ms.assetid: 9fce6b33-394c-47d2-9d02-7b0dadaa1736
ms.date: 12/05/2018
ms.keywords: IETFilter, IETFilter interface [Microsoft TV Technologies], IETFilter interface [Microsoft TV Technologies],described, IETFilterInterface, encdec/IETFilter, mstv.ietfilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IETFilter
 - encdec/IETFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilter
---

# IETFilter interface


## -description

The <b>IETFilter</b> interface is exposed by the Encrypter/Tagger filter. Most applications will not have to use this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IETFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IETFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IETFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilter-get_evalratobjok">get_EvalRatObjOK</a>
</td>
<td align="left" width="63%">
Queries whether the <b>EvalRat</b> object was created successfully.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilter-getcurrlicenseexpdate">GetCurrLicenseExpDate</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilter-getcurrrating">GetCurrRating</a>
</td>
<td align="left" width="63%">
Retrieves the current rating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilter-getlasterrorcode">GetLastErrorCode</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-ietfilter-setrecordingon">SetRecordingOn</a>
</td>
<td align="left" width="63%">
Signals to the Encrypter/Tagger filter that the Video Control is about to start or stop recording.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IETFilter)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>

