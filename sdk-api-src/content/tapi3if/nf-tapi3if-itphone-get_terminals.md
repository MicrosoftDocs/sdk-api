---
UID: NF:tapi3if.ITPhone.get_Terminals
title: ITPhone::get_Terminals (tapi3if.h)
description: The get_Terminals method retrieves a collection of terminals that are associated with the phone. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_Terminals method","ITPhone.get_Terminals","ITPhone::get_Terminals","_tapi3_itphone_get_terminals","get_Terminals","get_Terminals method [TAPI 2.2]","get_Terminals method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_terminals","tapi3if/ITPhone::get_Terminals"]
old-location: tapi3\itphone_get_terminals.htm
tech.root: tapi3
ms.assetid: 09e5921c-c7da-40fc-902a-1e22ebe19b0a
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Terminals method, ITPhone.get_Terminals, ITPhone::get_Terminals, _tapi3_itphone_get_terminals, get_Terminals, get_Terminals method [TAPI 2.2], get_Terminals method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_terminals, tapi3if/ITPhone::get_Terminals
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
 - ITPhone::get_Terminals
 - tapi3if/ITPhone::get_Terminals
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
 - ITPhone.get_Terminals
---

# ITPhone::get_Terminals


## -description

The 
<b>get_Terminals</b> method retrieves a collection of terminals that are associated with the phone. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

## -parameters

### -param pAddress [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface.

### -param pTerminals [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointers.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If no terminals are associated with the phone, this method produces an empty collection and returns S_OK.

The application does not have to call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before calling 
<b>get_Terminals</b>. This is because the implementation of the phone object can open the phone and call 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITPhone::get_Terminals</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>