---
UID: NN:tapi3if.ITLocationInfo
title: ITLocationInfo (tapi3if.h)
description: The ITLocationInfo interface is used to get information related to the location of the calling party. This is the location information that is entered by using the Telephony applet under the Control Panel.
helpviewer_keywords: ["ITLocationInfo","ITLocationInfo interface [TAPI 2.2]","ITLocationInfo interface [TAPI 2.2]","described","_tapi3_itlocationinfo","tapi3.itlocationinfo","tapi3if/ITLocationInfo"]
old-location: tapi3\itlocationinfo.htm
tech.root: tapi3
ms.assetid: 0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4
ms.date: 12/05/2018
ms.keywords: ITLocationInfo, ITLocationInfo interface [TAPI 2.2], ITLocationInfo interface [TAPI 2.2],described, _tapi3_itlocationinfo, tapi3.itlocationinfo, tapi3if/ITLocationInfo
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
 - ITLocationInfo
 - tapi3if/ITLocationInfo
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
 - ITLocationInfo
---

# ITLocationInfo interface


## -description

The 
<b>ITLocationInfo</b> interface is used to get information related to the location of the calling party. This is the location information that is entered by using the Telephony applet under the Control Panel.

An 
<b>ITLocationInfo</b> interface pointer is obtained by using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratelocations">ITAddressTranslation::EnumerateLocations</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_locations">ITAddressTranslation::get_Locations</a>. There can be more than one location entries in the Telephony applet. If so, 
<b>EnumerateLocations</b> and 
<b>get_Locations</b> will return them all. However, only one of them is the current location, and TAPI uses that one as the address translation context when 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress">ITAddressTranslation::TranslateAddress</a> is called.

The 
<b>ITLocationInfo</b> interface is a COM wrapper for the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -inheritance

The <b>ITLocationInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITLocationInfo</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratelocations">ITAddressTranslation::EnumerateLocations</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress">ITAddressTranslation::TranslateAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_locations">ITAddressTranslation::get_Locations</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>
