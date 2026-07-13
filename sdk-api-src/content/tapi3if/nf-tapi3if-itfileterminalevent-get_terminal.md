---
UID: NF:tapi3if.ITFileTerminalEvent.get_Terminal
title: ITFileTerminalEvent::get_Terminal (tapi3if.h)
description: The get_Terminal method returns the file terminal that generated this event.
helpviewer_keywords: ["ITFileTerminalEvent interface [TAPI 2.2]","get_Terminal method","ITFileTerminalEvent.get_Terminal","ITFileTerminalEvent::get_Terminal","_tapi3_itfileterminalevent_get_terminal","get_Terminal","get_Terminal method [TAPI 2.2]","get_Terminal method [TAPI 2.2]","ITFileTerminalEvent interface","tapi3.itfileterminalevent_get_terminal","tapi3if/ITFileTerminalEvent::get_Terminal"]
old-location: tapi3\itfileterminalevent_get_terminal.htm
tech.root: tapi3
ms.assetid: 515d9c65-1c24-485a-b7e4-1640e4e8c382
ms.date: 12/05/2018
ms.keywords: ITFileTerminalEvent interface [TAPI 2.2],get_Terminal method, ITFileTerminalEvent.get_Terminal, ITFileTerminalEvent::get_Terminal, _tapi3_itfileterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITFileTerminalEvent interface, tapi3.itfileterminalevent_get_terminal, tapi3if/ITFileTerminalEvent::get_Terminal
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
 - ITFileTerminalEvent::get_Terminal
 - tapi3if/ITFileTerminalEvent::get_Terminal
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
 - ITFileTerminalEvent.get_Terminal
---

# ITFileTerminalEvent::get_Terminal


## -description

The 
<b>get_Terminal</b> method returns the file terminal that generated this event.

## -parameters

### -param ppTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent">ITFileTerminalEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>