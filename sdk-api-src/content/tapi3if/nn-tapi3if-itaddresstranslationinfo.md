---
UID: NN:tapi3if.ITAddressTranslationInfo
title: ITAddressTranslationInfo (tapi3if.h)

description: Used to determine the address translation data.
old-location: tapi3\itaddresstranslationinfo.htm
tech.root: Tapi
ms.assetid: b59454a0-315f-4160-b969-d930c13bb4de

ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo, ITAddressTranslationInfo interface [TAPI 2.2], ITAddressTranslationInfo interface [TAPI 2.2],described, _tapi3_itaddresstranslationinfo, tapi3.itaddresstranslationinfo, tapi3if/ITAddressTranslationInfo
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITAddressTranslationInfo"
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
 - ITAddressTranslationInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressTranslationInfo interface


## -description


The 
<b>ITAddressTranslationInfo</b> interface is used to determine the address translation data. To obtain a pointer to it, call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress">ITAddressTranslation::TranslateAddress</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressTranslationInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressTranslationInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddressTranslationInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_currentcountrycode">get_CurrentCountryCode</a>
</td>
<td align="left" width="63%">
Gets the current country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_destinationcountrycode">get_DestinationCountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code for the call destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_dialablestring">get_DialableString</a>
</td>
<td align="left" width="63%">
Gets a string that contains a number to be dialed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_displayablestring">get_DisplayableString</a>
</td>
<td align="left" width="63%">
Gets a string that contains a displayable version of the number to be dialed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults">get_TranslationResults</a>
</td>
<td align="left" width="63%">
Gets the translated dialed number calling address.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>
 

 

