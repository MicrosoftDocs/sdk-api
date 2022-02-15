---
UID: NF:tapi3if.ITPhone.EnumerateTerminals
title: ITPhone::EnumerateTerminals (tapi3if.h)
description: The EnumerateTerminals method retrieves an enumeration of terminals that are associated with the phone. The application does not have to call ITPhone::Open before executing this method.
helpviewer_keywords: ["EnumerateTerminals","EnumerateTerminals method [TAPI 2.2]","EnumerateTerminals method [TAPI 2.2]","ITPhone interface","ITPhone interface [TAPI 2.2]","EnumerateTerminals method","ITPhone.EnumerateTerminals","ITPhone::EnumerateTerminals","_tapi3_itphone_enumerateterminals","tapi3.itphone_enumerateterminals","tapi3if/ITPhone::EnumerateTerminals"]
old-location: tapi3\itphone_enumerateterminals.htm
tech.root: tapi3
ms.assetid: 87c756e3-abd0-4dff-b815-ff7dd60902f7
ms.date: 12/05/2018
ms.keywords: EnumerateTerminals, EnumerateTerminals method [TAPI 2.2], EnumerateTerminals method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],EnumerateTerminals method, ITPhone.EnumerateTerminals, ITPhone::EnumerateTerminals, _tapi3_itphone_enumerateterminals, tapi3.itphone_enumerateterminals, tapi3if/ITPhone::EnumerateTerminals
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
 - ITPhone::EnumerateTerminals
 - tapi3if/ITPhone::EnumerateTerminals
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
 - ITPhone.EnumerateTerminals
---

# ITPhone::EnumerateTerminals


## -description

The 
<b>EnumerateTerminals</b> method retrieves an enumeration of terminals that are associated with the phone. The application does not have to call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before executing this method.

## -parameters

### -param pAddress [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface.

### -param ppEnumTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> interface that enumerates terminals.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If no terminals are associated with the phone, this method produces an empty enumeration and returns S_OK.

Although the 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> method before calling 
<b>EnumerateTerminals</b>. This is because the implementation of the phone object can open the phone and call 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetid">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> interface returned by <b>ITPhone::EnumerateTerminals</b>. The application must call <b>Release</b> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>