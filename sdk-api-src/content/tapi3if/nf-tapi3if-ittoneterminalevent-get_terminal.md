---
UID: NF:tapi3if.ITToneTerminalEvent.get_Terminal
title: ITToneTerminalEvent::get_Terminal (tapi3if.h)
description: The get_Terminal method returns an ITTerminal pointer for the tone terminal on which the event occurred.
helpviewer_keywords: ["ITToneTerminalEvent interface [TAPI 2.2]","get_Terminal method","ITToneTerminalEvent.get_Terminal","ITToneTerminalEvent::get_Terminal","_tapi3_ittoneterminalevent_get_terminal","get_Terminal","get_Terminal method [TAPI 2.2]","get_Terminal method [TAPI 2.2]","ITToneTerminalEvent interface","tapi3.ittoneterminalevent_get_terminal","tapi3if/ITToneTerminalEvent::get_Terminal"]
old-location: tapi3\ittoneterminalevent_get_terminal.htm
tech.root: tapi3
ms.assetid: 3358e219-fde9-4b60-bf75-c6d8c42a51ea
ms.date: 12/05/2018
ms.keywords: ITToneTerminalEvent interface [TAPI 2.2],get_Terminal method, ITToneTerminalEvent.get_Terminal, ITToneTerminalEvent::get_Terminal, _tapi3_ittoneterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITToneTerminalEvent interface, tapi3.ittoneterminalevent_get_terminal, tapi3if/ITToneTerminalEvent::get_Terminal
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
 - ITToneTerminalEvent::get_Terminal
 - tapi3if/ITToneTerminalEvent::get_Terminal
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
 - ITToneTerminalEvent.get_Terminal
---

# ITToneTerminalEvent::get_Terminal


## -description

The 
<b>get_Terminal</b> method returns an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> pointer for the tone terminal on which the event occurred.

## -parameters

### -param ppTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITToneTerminalEvent::get_Terminal</b>. The application must call <b>Release</b> on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent">ITToneTerminalEvent</a>