---
UID: NN:encdec.IDTFilter3
title: IDTFilter3 (encdec.h)
description: The IDTFilter3 interface extends the IDTFilter2 interface and is exposed by the Decrypter/Detagger filter.helpviewer_keywords: ["IDTFilter3","IDTFilter3 interface [Microsoft TV Technologies]","IDTFilter3 interface [Microsoft TV Technologies]","described","IDTFilter3Interface","encdec/IDTFilter3","mstv.idtfilter3"]
old-location: mstv\idtfilter3.htm
tech.root: mstv
ms.assetid: 88e42006-c387-41b5-a013-e968da0d918b
ms.date: 12/05/2018
ms.keywords: IDTFilter3, IDTFilter3 interface [Microsoft TV Technologies], IDTFilter3 interface [Microsoft TV Technologies],described, IDTFilter3Interface, encdec/IDTFilter3, mstv.idtfilter3
f1_keywords:
- encdec/IDTFilter3
dev_langs:
- c++
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
- encdec.h
api_name:
- IDTFilter3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilter3 interface


## -description



The <b>IDTFilter3</b> interface extends the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter2">IDTFilter2</a> interface and is exposed by the Decrypter/Detagger filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDTFilter3</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter2">IDTFilter2</a>. <b>IDTFilter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDTFilter3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter3-getprotectiontype">GetProtectionType</a>
</td>
<td align="left" width="63%">
Retrieves the type of content protection that is currently in effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter3-licensehasexpirationdate">LicenseHasExpirationDate</a>
</td>
<td align="left" width="63%">
Queries whether the license for the content has an expiration date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nf-encdec-idtfilter3-setrights">SetRights</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDTFilter3)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter2">IDTFilter2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-interfaces">TV Ratings Interfaces</a>
 

 

