---
UID: NF:dvbsiparser.IDvbParentalRatingDescriptor.GetRecordRating
title: IDvbParentalRatingDescriptor::GetRecordRating
author: windows-sdk-content
description: Gets a code that indicates the age-based rating for a Digital Video Broadcast (DVB) broadcast from a DVB parental rating descriptor.
old-location: mstv\idvbparentalratingdescriptor_getrecordrating.htm
tech.root: mstv
ms.assetid: 1b439669-6458-46d3-882d-5f20f2f22f23
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordRating, GetRecordRating method [Microsoft TV Technologies], GetRecordRating method [Microsoft TV Technologies],IDvbParentalRatingDescriptor interface, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],GetRecordRating method, IDvbParentalRatingDescriptor.GetRecordRating, IDvbParentalRatingDescriptor::GetRecordRating, dvbsiparser/IDvbParentalRatingDescriptor::GetRecordRating, mstv.idvbparentalratingdescriptor_getrecordrating
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbParentalRatingDescriptor.GetRecordRating
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbParentalRatingDescriptor::GetRecordRating


## -description


 Gets a code that indicates the age-based rating for a Digital Video Broadcast (DVB) broadcast from a DVB parental rating descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/72dcfb91-4137-4149-b30d-2551cb209688">IDvbParentalRatingDescriptor::GetCountOfRecords</a>.


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/667ef815-ef22-4dd1-9457-49af674b24ab">IDvbParentalRatingDescriptor</a>
 

 

