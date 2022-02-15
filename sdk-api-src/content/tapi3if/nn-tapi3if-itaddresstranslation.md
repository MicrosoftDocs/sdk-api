---
UID: NN:tapi3if.ITAddressTranslation
title: ITAddressTranslation (tapi3if.h)
description: The ITAddressTranslation interface provides methods that allow translation of a calling address into a different format. For example, an application may need to translate an address from canonical to dialable prior to making a call.
helpviewer_keywords: ["ITAddressTranslation","ITAddressTranslation interface [TAPI 2.2]","ITAddressTranslation interface [TAPI 2.2]","described","_tapi3_itaddresstranslation","tapi3.itaddresstranslation","tapi3if/ITAddressTranslation"]
old-location: tapi3\itaddresstranslation.htm
tech.root: tapi3
ms.assetid: e1cd88f1-1ed7-4e7f-a745-9a9c4af69317
ms.date: 12/05/2018
ms.keywords: ITAddressTranslation, ITAddressTranslation interface [TAPI 2.2], ITAddressTranslation interface [TAPI 2.2],described, _tapi3_itaddresstranslation, tapi3.itaddresstranslation, tapi3if/ITAddressTranslation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAddressTranslation
 - tapi3if/ITAddressTranslation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslation
---

# ITAddressTranslation interface


## -description

The 
<b>ITAddressTranslation</b> interface provides methods that allow translation of a calling address into a different format. For example, an application may need to translate an address from canonical to dialable prior to making a call.

The most common use of this interface is to obtain the <i>pDestAddress</i> string needed for 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>. The addresses to be translated are mainly phone numbers in canonical format.

The 
<b>ITAddressTranslation</b> interface is exposed on the 
<a href="/windows/desktop/Tapi/address-object">Address Object</a>. A pointer can be obtained by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.

For additional information, see 
<a href="/windows/desktop/Tapi/initiate-a-session-ovr">Address Translation</a> and 
<a href="/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>.

## -inheritance

The <b>ITAddressTranslation</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressTranslation</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/Tapi/initiate-a-session-ovr">Address Translation</a>



<a href="/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>
