---
UID: NN:tapi3if.ITAddressTranslationInfo
title: ITAddressTranslationInfo (tapi3if.h)
description: Used to determine the address translation data.
helpviewer_keywords: ["ITAddressTranslationInfo","ITAddressTranslationInfo interface [TAPI 2.2]","ITAddressTranslationInfo interface [TAPI 2.2]","described","_tapi3_itaddresstranslationinfo","tapi3.itaddresstranslationinfo","tapi3if/ITAddressTranslationInfo"]
old-location: tapi3\itaddresstranslationinfo.htm
tech.root: tapi3
ms.assetid: b59454a0-315f-4160-b969-d930c13bb4de
ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo, ITAddressTranslationInfo interface [TAPI 2.2], ITAddressTranslationInfo interface [TAPI 2.2],described, _tapi3_itaddresstranslationinfo, tapi3.itaddresstranslationinfo, tapi3if/ITAddressTranslationInfo
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
 - ITAddressTranslationInfo
 - tapi3if/ITAddressTranslationInfo
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
 - ITAddressTranslationInfo
---

# ITAddressTranslationInfo interface


## -description

The 
<b>ITAddressTranslationInfo</b> interface is used to determine the address translation data. To obtain a pointer to it, call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress">ITAddressTranslation::TranslateAddress</a>.

## -inheritance

The <b>ITAddressTranslationInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressTranslationInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">lineTranslateAddress</a>
