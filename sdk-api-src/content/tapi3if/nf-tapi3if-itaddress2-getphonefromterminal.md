---
UID: NF:tapi3if.ITAddress2.GetPhoneFromTerminal
title: ITAddress2::GetPhoneFromTerminal (tapi3if.h)
description: The GetPhoneFromTerminal method returns the phone object associated with the terminal. Only one phone can be associated with a terminal.
helpviewer_keywords: ["GetPhoneFromTerminal","GetPhoneFromTerminal method [TAPI 2.2]","GetPhoneFromTerminal method [TAPI 2.2]","ITAddress2 interface","ITAddress2 interface [TAPI 2.2]","GetPhoneFromTerminal method","ITAddress2.GetPhoneFromTerminal","ITAddress2::GetPhoneFromTerminal","_tapi3_itaddress2_getphonefromterminal","tapi3.itaddress2_getphonefromterminal","tapi3if/ITAddress2::GetPhoneFromTerminal"]
old-location: tapi3\itaddress2_getphonefromterminal.htm
tech.root: tapi3
ms.assetid: 0d3873ad-ce3d-4b4c-907f-9c0dbf0ef206
ms.date: 12/05/2018
ms.keywords: GetPhoneFromTerminal, GetPhoneFromTerminal method [TAPI 2.2], GetPhoneFromTerminal method [TAPI 2.2],ITAddress2 interface, ITAddress2 interface [TAPI 2.2],GetPhoneFromTerminal method, ITAddress2.GetPhoneFromTerminal, ITAddress2::GetPhoneFromTerminal, _tapi3_itaddress2_getphonefromterminal, tapi3.itaddress2_getphonefromterminal, tapi3if/ITAddress2::GetPhoneFromTerminal
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
 - ITAddress2::GetPhoneFromTerminal
 - tapi3if/ITAddress2::GetPhoneFromTerminal
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
 - ITAddress2.GetPhoneFromTerminal
---

# ITAddress2::GetPhoneFromTerminal


## -description

The 
<b>GetPhoneFromTerminal</b> method returns the phone object associated with the terminal. Only one phone can be associated with a terminal.

## -parameters

### -param pTerminal [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

### -param ppPhone [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>