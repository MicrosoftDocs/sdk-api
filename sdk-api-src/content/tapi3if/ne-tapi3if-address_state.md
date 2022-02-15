---
UID: NE:tapi3if.ADDRESS_STATE
title: ADDRESS_STATE (tapi3if.h)
description: The ADDRESS_STATE enum is used by the ITAddress::get_State method to check the address state.
helpviewer_keywords: ["ADDRESS_STATE","ADDRESS_STATE enumeration [TAPI 2.2]","AS_INSERVICE","AS_OUTOFSERVICE","_tapi3_address_state","tapi3.address_state","tapi3if/ADDRESS_STATE","tapi3if/AS_INSERVICE","tapi3if/AS_OUTOFSERVICE"]
old-location: tapi3\address_state.htm
tech.root: tapi3
ms.assetid: 7c79bd68-5f1d-4796-a16b-fd786345cffd
ms.date: 12/05/2018
ms.keywords: ADDRESS_STATE, ADDRESS_STATE enumeration [TAPI 2.2], AS_INSERVICE, AS_OUTOFSERVICE, _tapi3_address_state, tapi3.address_state, tapi3if/ADDRESS_STATE, tapi3if/AS_INSERVICE, tapi3if/AS_OUTOFSERVICE
req.header: tapi3if.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADDRESS_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADDRESS_STATE
 - tapi3if/ADDRESS_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - ADDRESS_STATE
---

# ADDRESS_STATE enumeration


## -description

The 
<b>ADDRESS_STATE</b> enum is used by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_state">ITAddress::get_State</a> method to check the address state.

## -enum-fields

### -field AS_INSERVICE:0

Normal state; the address can be used.

### -field AS_OUTOFSERVICE

The address is temporarily out of service, but may go back into service at some time.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_state">ITAddress::get_State</a>
