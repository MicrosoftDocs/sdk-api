---
UID: NE:tapi3if.TERMINAL_MEDIA_STATE
title: TERMINAL_MEDIA_STATE (tapi3if.h)
description: The TERMINAL_MEDIA_STATE enum indicates the state of a file terminal.
helpviewer_keywords: ["TERMINAL_MEDIA_STATE","TERMINAL_MEDIA_STATE enumeration [TAPI 2.2]","TMS_ACTIVE","TMS_IDLE","TMS_LASTITEM","TMS_PAUSED","_tapi3_terminal_media_state","tapi3.terminal_media_state","tapi3if/TERMINAL_MEDIA_STATE","tapi3if/TMS_ACTIVE","tapi3if/TMS_IDLE","tapi3if/TMS_LASTITEM","tapi3if/TMS_PAUSED"]
old-location: tapi3\terminal_media_state.htm
tech.root: tapi3
ms.assetid: 9cc07684-9804-41ac-bc25-f37f6ae00280
ms.date: 12/05/2018
ms.keywords: TERMINAL_MEDIA_STATE, TERMINAL_MEDIA_STATE enumeration [TAPI 2.2], TMS_ACTIVE, TMS_IDLE, TMS_LASTITEM, TMS_PAUSED, _tapi3_terminal_media_state, tapi3.terminal_media_state, tapi3if/TERMINAL_MEDIA_STATE, tapi3if/TMS_ACTIVE, tapi3if/TMS_IDLE, tapi3if/TMS_LASTITEM, tapi3if/TMS_PAUSED
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
req.typenames: TERMINAL_MEDIA_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TERMINAL_MEDIA_STATE
 - tapi3if/TERMINAL_MEDIA_STATE
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
 - TERMINAL_MEDIA_STATE
---

# TERMINAL_MEDIA_STATE enumeration


## -description

The 
<b>TERMINAL_MEDIA_STATE</b> enum indicates the state of a file terminal.

## -enum-fields

### -field TMS_IDLE:0

The file terminal is idle.

### -field TMS_ACTIVE

The file terminal is active.

### -field TMS_PAUSED

The file terminal is paused.

### -field TMS_LASTITEM:TMS_PAUSED

Last item in this enum.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itfileterminalevent-get_state">ITFileTerminalEvent::get_State</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-get_mediastate">ITMediaControl::get_MediaState</a>
