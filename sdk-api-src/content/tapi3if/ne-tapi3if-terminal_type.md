---
UID: NE:tapi3if.TERMINAL_TYPE
title: TERMINAL_TYPE (tapi3if.h)
description: The TERMINAL_TYPE enum describes the type of the terminal. This enum is returned by the ITTerminal::get_TerminalType method.
helpviewer_keywords: ["TERMINAL_TYPE","TERMINAL_TYPE enumeration [TAPI 2.2]","TT_DYNAMIC","TT_STATIC","_tapi3_terminal_type","tapi3.terminal_type","tapi3if/TERMINAL_TYPE","tapi3if/TT_DYNAMIC","tapi3if/TT_STATIC"]
old-location: tapi3\terminal_type.htm
tech.root: tapi3
ms.assetid: 43d08be3-c09b-4c74-ad71-6b452850d2e0
ms.date: 12/05/2018
ms.keywords: TERMINAL_TYPE, TERMINAL_TYPE enumeration [TAPI 2.2], TT_DYNAMIC, TT_STATIC, _tapi3_terminal_type, tapi3.terminal_type, tapi3if/TERMINAL_TYPE, tapi3if/TT_DYNAMIC, tapi3if/TT_STATIC
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
req.typenames: TERMINAL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TERMINAL_TYPE
 - tapi3if/TERMINAL_TYPE
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
 - TERMINAL_TYPE
---

# TERMINAL_TYPE enumeration


## -description

The 
<b>TERMINAL_TYPE</b> enum describes the type of the terminal. This enum is returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype">ITTerminal::get_TerminalType</a> method.

## -enum-fields

### -field TT_STATIC:0

A static terminal is a terminal that cannot be created and usually refers to hardware device. TAPI enumerates these terminals.

### -field TT_DYNAMIC

A terminal type that can be created. The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">ITTerminalSupport::CreateTerminal</a> to use this type of terminal.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype">ITTerminal::get_TerminalType</a>
