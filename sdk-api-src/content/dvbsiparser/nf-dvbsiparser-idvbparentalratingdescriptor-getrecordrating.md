---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

