---
UID: NF:tapi3if.ITASRTerminalEvent.get_Terminal
title: ITASRTerminalEvent::get_Terminal (tapi3if.h)
description: The get_Terminal method returns a pointer to the ITTerminal interface for the terminal on which the event occurred.
helpviewer_keywords: ["ITASRTerminalEvent interface [TAPI 2.2]","get_Terminal method","ITASRTerminalEvent.get_Terminal","ITASRTerminalEvent::get_Terminal","_tapi3_itasrterminalevent_get_terminal","get_Terminal","get_Terminal method [TAPI 2.2]","get_Terminal method [TAPI 2.2]","ITASRTerminalEvent interface","tapi3.itasrterminalevent_get_terminal","tapi3if/ITASRTerminalEvent::get_Terminal"]
old-location: tapi3\itasrterminalevent_get_terminal.htm
tech.root: tapi3
ms.assetid: 1cde7b16-f825-4591-9947-6ad03cbd14c6
ms.date: 12/05/2018
ms.keywords: ITASRTerminalEvent interface [TAPI 2.2],get_Terminal method, ITASRTerminalEvent.get_Terminal, ITASRTerminalEvent::get_Terminal, _tapi3_itasrterminalevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITASRTerminalEvent interface, tapi3.itasrterminalevent_get_terminal, tapi3if/ITASRTerminalEvent::get_Terminal
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
 - ITASRTerminalEvent::get_Terminal
 - tapi3if/ITASRTerminalEvent::get_Terminal
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
 - ITASRTerminalEvent.get_Terminal
---

# ITASRTerminalEvent::get_Terminal


## -description

The 
<b>get_Terminal</b> method returns a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface for the terminal on which the event occurred.

## -parameters

### -param ppTerminal [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent">ITASRTerminalEvent</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>