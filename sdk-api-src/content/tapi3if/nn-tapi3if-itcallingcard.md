---
UID: NN:tapi3if.ITCallingCard
title: ITCallingCard (tapi3if.h)
description: The ITCallingCard interface provides methods to retrieve information concerning telephony calling cards.
old-location: tapi3\itcallingcard.htm
tech.root: Tapi
ms.assetid: 09787cd2-56b5-4ed2-8783-f3c53ce2cc66
ms.date: 12/05/2018
ms.keywords: ITCallingCard, ITCallingCard interface [TAPI 2.2], ITCallingCard interface [TAPI 2.2],described, _tapi3_itcallingcard, tapi3.itcallingcard, tapi3if/ITCallingCard
f1_keywords:
- tapi3if/ITCallingCard
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITCallingCard
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallingCard interface


## -description


The 
<b>ITCallingCard</b> interface provides methods to retrieve information concerning telephony calling cards.

An 
<b>ITCallingCard</b> interface pointer can be obtained using 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_callingcards">ITAddressTranslation::get_CallingCards</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">ITAddressTranslation::EnumerateCallingCards</a>.

<b>TAPI 2.1 Cross-Reference: </b>The information obtainable using this interface parallels that contained in the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a> structure. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> function returns a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure. The <b>dwCardListOffset</b> member of this structure points to a list of 
<b>LINECARDENTRY</b> structures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallingCard</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallingCard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallingCard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_cardname">get_CardName</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the calling card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_internationaldialingrule">get_InternationalDialingRule</a>
</td>
<td align="left" width="63%">
Gets the international dialing rules for this calling card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_longdistancedialingrule">get_LongDistanceDialingRule</a>
</td>
<td align="left" width="63%">
Gets the long distance dialing rules for this calling card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_numberofdigits">get_NumberOfDigits</a>
</td>
<td align="left" width="63%">
Gets the number of digits in the existing card number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_options">get_Options</a>
</td>
<td align="left" width="63%">
Gets the translation options for this address and card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_permanentcardid">get_PermanentCardID</a>
</td>
<td align="left" width="63%">
Gets the permanent calling card identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallingcard-get_sameareadialingrule">get_SameAreaDialingRule</a>
</td>
<td align="left" width="63%">
Gets the dialing rules for calls within the same area code.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">ITAddressTranslation::EnumerateCallingCards</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_callingcards">ITAddressTranslation::get_CallingCards</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>
 

 

