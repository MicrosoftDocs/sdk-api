---
UID: NE:tapi3if.TERMINAL_STATE
title: TERMINAL_STATE (tapi3if.h)
description: The TERMINAL_STATE enum describes the current state of a terminal device. This enum is returned by the ITTerminal::get_State method.
helpviewer_keywords: ["TERMINAL_STATE","TERMINAL_STATE enumeration [TAPI 2.2]","TS_INUSE","TS_NOTINUSE","_tapi3_terminal_state","tapi3.terminal_state","tapi3if/TERMINAL_STATE","tapi3if/TS_INUSE","tapi3if/TS_NOTINUSE"]
old-location: tapi3\terminal_state.htm
tech.root: tapi3
ms.assetid: 310c41f5-dfe7-491d-8669-87a98694f5b7
ms.date: 12/05/2018
ms.keywords: TERMINAL_STATE, TERMINAL_STATE enumeration [TAPI 2.2], TS_INUSE, TS_NOTINUSE, _tapi3_terminal_state, tapi3.terminal_state, tapi3if/TERMINAL_STATE, tapi3if/TS_INUSE, tapi3if/TS_NOTINUSE
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
req.typenames: TERMINAL_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TERMINAL_STATE
 - tapi3if/TERMINAL_STATE
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
 - TERMINAL_STATE
---

# TERMINAL_STATE enumeration


## -description

The 
<b>TERMINAL_STATE</b> enum describes the current state of a terminal device. This enum is returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_state">ITTerminal::get_State</a> method.

## -enum-fields

### -field TS_INUSE:0

The terminal is currently in use.

### -field TS_NOTINUSE

The terminal is not currently in use.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_state">ITTerminal::get_State</a>
