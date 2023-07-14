---
UID: NF:dvbsiparser.IDvbParentalRatingDescriptor.GetRecordRating
title: IDvbParentalRatingDescriptor::GetRecordRating (dvbsiparser.h)
description: Gets a code that indicates the age-based rating for a Digital Video Broadcast (DVB) broadcast from a DVB parental rating descriptor.
helpviewer_keywords: ["GetRecordRating","GetRecordRating method [Microsoft TV Technologies]","GetRecordRating method [Microsoft TV Technologies]","IDvbParentalRatingDescriptor interface","IDvbParentalRatingDescriptor interface [Microsoft TV Technologies]","GetRecordRating method","IDvbParentalRatingDescriptor.GetRecordRating","IDvbParentalRatingDescriptor::GetRecordRating","dvbsiparser/IDvbParentalRatingDescriptor::GetRecordRating","mstv.idvbparentalratingdescriptor_getrecordrating"]
old-location: mstv\idvbparentalratingdescriptor_getrecordrating.htm
tech.root: mstv
ms.assetid: 1b439669-6458-46d3-882d-5f20f2f22f23
ms.date: 12/05/2018
ms.keywords: GetRecordRating, GetRecordRating method [Microsoft TV Technologies], GetRecordRating method [Microsoft TV Technologies],IDvbParentalRatingDescriptor interface, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],GetRecordRating method, IDvbParentalRatingDescriptor.GetRecordRating, IDvbParentalRatingDescriptor::GetRecordRating, dvbsiparser/IDvbParentalRatingDescriptor::GetRecordRating, mstv.idvbparentalratingdescriptor_getrecordrating
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IDvbParentalRatingDescriptor::GetRecordRating
 - dvbsiparser/IDvbParentalRatingDescriptor::GetRecordRating
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbParentalRatingDescriptor.GetRecordRating
---

# IDvbParentalRatingDescriptor::GetRecordRating


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets a code that indicates the age-based rating for a Digital Video Broadcast (DVB) broadcast from a DVB parental rating descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbparentalratingdescriptor-getcountofrecords">IDvbParentalRatingDescriptor::GetCountOfRecords</a>.

### -param pszCountryCode

Receives the ISO 3166 country code from the parental rating descriptor.

### -param pbVal [out]

Gets the rating code. This can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01-0x0F</dt>
</dl>
</td>
<td width="60%">
 Minimum age is 3 years. For example, 0x0A implies that end users should be at least 13 years old.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x10-0xFF</dt>
</dl>
</td>
<td width="60%">
Broadcaster defined.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbparentalratingdescriptor">IDvbParentalRatingDescriptor</a>