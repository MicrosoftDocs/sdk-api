---
UID: NN:tapi3if.ITAddressTranslation
title: ITAddressTranslation (tapi3if.h)
description: The ITAddressTranslation interface provides methods that allow translation of a calling address into a different format. For example, an application may need to translate an address from canonical to dialable prior to making a call.
helpviewer_keywords: ["ITAddressTranslation","ITAddressTranslation interface [TAPI 2.2]","ITAddressTranslation interface [TAPI 2.2]","described","_tapi3_itaddresstranslation","tapi3.itaddresstranslation","tapi3if/ITAddressTranslation"]
old-location: tapi3\itaddresstranslation.htm
tech.root: Tapi
ms.assetid: e1cd88f1-1ed7-4e7f-a745-9a9c4af69317
ms.date: 12/05/2018
ms.keywords: ITAddressTranslation, ITAddressTranslation interface [TAPI 2.2], ITAddressTranslation interface [TAPI 2.2],described, _tapi3_itaddresstranslation, tapi3.itaddresstranslation, tapi3if/ITAddressTranslation
f1_keywords:
- tapi3if/ITAddressTranslation
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
- ITAddressTranslation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressTranslation interface


## -description


The 
<b>ITAddressTranslation</b> interface provides methods that allow translation of a calling address into a different format. For example, an application may need to translate an address from canonical to dialable prior to making a call.

The most common use of this interface is to obtain the <i>pDestAddress</i> string needed for 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>. The addresses to be translated are mainly phone numbers in canonical format.

The 
<b>ITAddressTranslation</b> interface is exposed on the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>. A pointer can be obtained by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.

For additional information, see 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/initiate-a-session-ovr">Address Translation</a> and 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressTranslation</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressTranslation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddressTranslation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">EnumerateCallingCards</a>
</td>
<td align="left" width="63%">
Enumerates calling cards associated with the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratelocations">EnumerateLocations</a>
</td>
<td align="left" width="63%">
Enumerates the currently available address locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_callingcards">get_CallingCards</a>
</td>
<td align="left" width="63%">
Creates a collection of calling cards associated with the address. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_locations">get_Locations</a>
</td>
<td align="left" width="63%">
Creates a collection of currently available address locations. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress">TranslateAddress</a>
</td>
<td align="left" width="63%">
Creates the address translation information interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translatedialog">TranslateDialog</a>
</td>
<td align="left" width="63%">
Invokes the control panel's telephony applet.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/initiate-a-session-ovr">Address Translation</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>
 

 

