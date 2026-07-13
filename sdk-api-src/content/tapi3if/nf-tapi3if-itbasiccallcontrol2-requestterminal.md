---
UID: NF:tapi3if.ITBasicCallControl2.RequestTerminal
title: ITBasicCallControl2::RequestTerminal (tapi3if.h)
description: The RequestTerminal method gets a suitable terminal, given the class, media, and direction required.
helpviewer_keywords: ["ITBasicCallControl2 interface [TAPI 2.2]","RequestTerminal method","ITBasicCallControl2.RequestTerminal","ITBasicCallControl2::RequestTerminal","RequestTerminal","RequestTerminal method [TAPI 2.2]","RequestTerminal method [TAPI 2.2]","ITBasicCallControl2 interface","_tapi3_itbasiccallcontrol2_requestterminal","tapi3.itbasiccallcontrol2_requestterminal","tapi3if/ITBasicCallControl2::RequestTerminal"]
old-location: tapi3\itbasiccallcontrol2_requestterminal.htm
tech.root: tapi3
ms.assetid: 20b7266c-8990-457c-94cf-18cc2bed6b21
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl2 interface [TAPI 2.2],RequestTerminal method, ITBasicCallControl2.RequestTerminal, ITBasicCallControl2::RequestTerminal, RequestTerminal, RequestTerminal method [TAPI 2.2], RequestTerminal method [TAPI 2.2],ITBasicCallControl2 interface, _tapi3_itbasiccallcontrol2_requestterminal, tapi3.itbasiccallcontrol2_requestterminal, tapi3if/ITBasicCallControl2::RequestTerminal
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
 - ITBasicCallControl2::RequestTerminal
 - tapi3if/ITBasicCallControl2::RequestTerminal
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
 - ITBasicCallControl2.RequestTerminal
---

# ITBasicCallControl2::RequestTerminal


## -description

The 
<b>RequestTerminal</b> method gets a suitable terminal, given the class, media, and direction required.

## -parameters

### -param bstrTerminalClassGUID [in]

The terminal class required for the call.

### -param lMediaType [in]

Bitwise ORed list of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a> required for the call.

### -param Direction [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor for the terminal.

### -param ppTerminal [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>AddRef</b> method is automatically called on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by this method. The application must call the <b>Release</b> method on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>