---
UID: NN:tapi3if.ITAddress
title: ITAddress (tapi3if.h)
description: The ITAddress interface is the base interface for the Address object. Applications use this interface to get information about and use the Address object.
helpviewer_keywords: ["ITAddress","ITAddress interface [TAPI 2.2]","ITAddress interface [TAPI 2.2]","described","_tapi3_itaddress","tapi3.itaddress","tapi3if/ITAddress"]
old-location: tapi3\itaddress.htm
tech.root: tapi3
ms.assetid: 93f2e4cf-013e-4064-88d5-69fddd458274
ms.date: 12/05/2018
ms.keywords: ITAddress, ITAddress interface [TAPI 2.2], ITAddress interface [TAPI 2.2],described, _tapi3_itaddress, tapi3.itaddress, tapi3if/ITAddress
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
 - ITAddress
 - tapi3if/ITAddress
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
 - ITAddress
---

# ITAddress interface


## -description

The 
<b>ITAddress</b> interface is the base interface for the Address object. Applications use this interface to get information about and use the 
<a href="/windows/desktop/Tapi/address-object">Address object</a>.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a> interface derives from the 
<b>ITAddress</b> interface. 
<b>ITAddress2</b> adds methods to the Address object in order to support phone devices. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumaddress-next">IEnumAddress::Next</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses">ITTapi::get_Addresses</a> methods create the 
<b>ITAddress</b> interface.

## -inheritance

The <b>ITAddress</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddress</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a>
