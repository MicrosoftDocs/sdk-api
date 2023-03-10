---
UID: NN:tapi3if.ITCallingCard
title: ITCallingCard (tapi3if.h)
description: The ITCallingCard interface provides methods to retrieve information concerning telephony calling cards.
helpviewer_keywords: ["ITCallingCard","ITCallingCard interface [TAPI 2.2]","ITCallingCard interface [TAPI 2.2]","described","_tapi3_itcallingcard","tapi3.itcallingcard","tapi3if/ITCallingCard"]
old-location: tapi3\itcallingcard.htm
tech.root: tapi3
ms.assetid: 09787cd2-56b5-4ed2-8783-f3c53ce2cc66
ms.date: 12/05/2018
ms.keywords: ITCallingCard, ITCallingCard interface [TAPI 2.2], ITCallingCard interface [TAPI 2.2],described, _tapi3_itcallingcard, tapi3.itcallingcard, tapi3if/ITCallingCard
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
 - ITCallingCard
 - tapi3if/ITCallingCard
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
 - ITCallingCard
---

# ITCallingCard interface


## -description

The 
<b>ITCallingCard</b> interface provides methods to retrieve information concerning telephony calling cards.

An 
<b>ITCallingCard</b> interface pointer can be obtained using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_callingcards">ITAddressTranslation::get_CallingCards</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">ITAddressTranslation::EnumerateCallingCards</a>.

<b>TAPI 2.1 Cross-Reference: </b>The information obtainable using this interface parallels that contained in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a> structure. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a> function returns a 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure. The <b>dwCardListOffset</b> member of this structure points to a list of 
<b>LINECARDENTRY</b> structures.

## -inheritance

The <b>ITCallingCard</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallingCard</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">ITAddressTranslation::EnumerateCallingCards</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_callingcards">ITAddressTranslation::get_CallingCards</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecardentry">LINECARDENTRY</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>
