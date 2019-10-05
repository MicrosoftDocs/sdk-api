---
UID: NN:encdec.IDTFilter2
title: IDTFilter2 (encdec.h)
author: windows-sdk-content
description: The IDTFilter2 interface extends the IDTFilter interface and is exposed by the Decrypter/Detagger filter.
old-location: mstv\idtfilter2.htm
tech.root: mstv
ms.assetid: 351c77ec-fb0c-4780-ad43-8ca6716b208f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDTFilter2, IDTFilter2 interface [Microsoft TV Technologies], IDTFilter2 interface [Microsoft TV Technologies],described, IDTFilter2Interface, encdec/IDTFilter2, mstv.idtfilter2
ms.topic: interface
f1_keywords: 
 - "encdec/IDTFilter2"
dev_langs:
 - c++
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - IDTFilter2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilter2 interface


## -description



The <b>IDTFilter2</b> interface extends the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter</a> interface and is exposed by the Decrypter/Detagger filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilter2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter</a>. <b>IDTFilter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDTFilter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter2-get_challengeurl">get_ChallengeUrl</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter2-getcurrlicenseexpdate">GetCurrLicenseExpDate</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter2-getlasterrorcode">GetLastErrorCode</a>
</td>
<td align="left" width="63%">
Returns the most recent error code from the Decrypter/Detagger filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilter2)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

