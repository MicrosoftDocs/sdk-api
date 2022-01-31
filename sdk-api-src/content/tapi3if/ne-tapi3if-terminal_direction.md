---
UID: NE:tapi3if.TERMINAL_DIRECTION
title: TERMINAL_DIRECTION (tapi3if.h)
description: The TERMINAL_DIRECTION enumeration is used to describe the direction of the media stream with respect to the local computer or the directional capabilities of a terminal.
helpviewer_keywords: ["TD_BIDIRECTIONAL","TD_CAPTURE","TD_MULTITRACK_MIXED","TD_NONE","TD_RENDER","TERMINAL_DIRECTION","TERMINAL_DIRECTION enumeration [TAPI 2.2]","_tapi3_terminal_direction","tapi3.terminal_direction","tapi3if/TD_BIDIRECTIONAL","tapi3if/TD_CAPTURE","tapi3if/TD_MULTITRACK_MIXED","tapi3if/TD_NONE","tapi3if/TD_RENDER","tapi3if/TERMINAL_DIRECTION"]
old-location: tapi3\terminal_direction.htm
tech.root: tapi3
ms.assetid: 55ef9df3-1b85-439b-8ecb-28e5069390b9
ms.date: 12/05/2018
ms.keywords: TD_BIDIRECTIONAL, TD_CAPTURE, TD_MULTITRACK_MIXED, TD_NONE, TD_RENDER, TERMINAL_DIRECTION, TERMINAL_DIRECTION enumeration [TAPI 2.2], _tapi3_terminal_direction, tapi3.terminal_direction, tapi3if/TD_BIDIRECTIONAL, tapi3if/TD_CAPTURE, tapi3if/TD_MULTITRACK_MIXED, tapi3if/TD_NONE, tapi3if/TD_RENDER, tapi3if/TERMINAL_DIRECTION
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
req.typenames: TERMINAL_DIRECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TERMINAL_DIRECTION
 - tapi3if/TERMINAL_DIRECTION
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
 - TERMINAL_DIRECTION
---

# TERMINAL_DIRECTION enumeration


## -description

The 
<b>TERMINAL_DIRECTION</b> enumeration is used to describe the direction of the media stream with respect to the local computer or the directional capabilities of a terminal.

## -enum-fields

### -field TD_CAPTURE:0

The stream is captured on the local computer, and the data is sent out to the remote end of the connection. When applied to a terminal, this means it can originate a stream.

### -field TD_RENDER

The stream is arriving from the remote end of the connection. When applied to a terminal, this means it can render a stream.

### -field TD_BIDIRECTIONAL

The terminal can handle either capture or render streams.

### -field TD_MULTITRACK_MIXED

Different tracks on the multi-track terminal may travel in different directions. For example, one track may specify <b>TD_RENDER</b> and another may specify <b>TD_CAPTURE</b>.

### -field TD_NONE

The terminal direction is unknown or not initialized.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_direction">ITStream::get_Direction</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">ITStreamControl::CreateStream</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_direction">ITTerminal::get_Direction</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itterminalmanager-createdynamicterminal">ITTerminalManager::CreateDynamicTerminal</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">ITTerminalSupport::CreateTerminal</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-getdefaultstaticterminal">ITTerminalSupport::GetDefaultStaticTerminal</a>
