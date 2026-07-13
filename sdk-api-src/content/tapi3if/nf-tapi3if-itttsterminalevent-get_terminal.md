---
UID: NF:tapi3if.ITTTSTerminalEvent.get_Terminal
title: ITTTSTerminalEvent::get_Terminal (tapi3if.h)
description: The get_Terminal method gets an ITTerminal interface pointer for the terminal object involved in the event.
helpviewer_keywords: ["ITTTSTerminalEvent interface [TAPI 2.2]","get_Terminal method","ITTTSTerminalEvent.get_Terminal","ITTTSTerminalEvent::get_Terminal","_tapi3_itttsterminalevent_get_terminal","get_Terminal","get_Terminal method [TAPI 2.2]","get_Terminal method [TAPI 2.2]","ITTTSTerminalEvent interface","tapi3.itttsterminalevent_get_terminal","tapi3if/ITTTSTerminalEvent::get_Terminal"]
old-location: tapi3\itttsterminalevent_get_terminal.htm
tech.root: tapi3
ms.assetid: ce37e074-8ce0-4fde-b16a-c85a9487f0db
ms.date: 12/05/2018
ms.keywords: ITTTSTerminalEvent interface [TAPI 2.2],get_Terminal method, ITTTSTerminalEvent.get_Terminal, ITTTSTerminalEvent::get_Terminal, _tapi3_itttsterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITTTSTerminalEvent interface, tapi3.itttsterminalevent_get_terminal, tapi3if/ITTTSTerminalEvent::get_Terminal
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
 - ITTTSTerminalEvent::get_Terminal
 - tapi3if/ITTTSTerminalEvent::get_Terminal
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
 - ITTTSTerminalEvent.get_Terminal
---

# ITTTSTerminalEvent::get_Terminal


## -description

The 
<b>get_Terminal</b> method gets an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointer for the terminal object involved in the event.

## -parameters

### -param ppTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITTTSTerminalEvent::get_Terminal</b>. The application must call <b>Release</b> on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent">ITTTSTerminalEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>