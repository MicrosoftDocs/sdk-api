---
UID: NF:tapi3if.ITMultiTrackTerminal.CreateTrackTerminal
title: ITMultiTrackTerminal::CreateTrackTerminal (tapi3if.h)
description: The CreateTrackTerminal method creates a multitrack terminal that can handle a given media type or types and media direction.
helpviewer_keywords: ["CreateTrackTerminal","CreateTrackTerminal method [TAPI 2.2]","CreateTrackTerminal method [TAPI 2.2]","ITMultiTrackTerminal interface","ITMultiTrackTerminal interface [TAPI 2.2]","CreateTrackTerminal method","ITMultiTrackTerminal.CreateTrackTerminal","ITMultiTrackTerminal::CreateTrackTerminal","_tapi3_itmultitrackterminal_createtrackterminal","tapi3.itmultitrackterminal_createtrackterminal","tapi3if/ITMultiTrackTerminal::CreateTrackTerminal"]
old-location: tapi3\itmultitrackterminal_createtrackterminal.htm
tech.root: tapi3
ms.assetid: fe853de7-5a22-4b49-aca0-e2e2a8c3e1d7
ms.date: 12/05/2018
ms.keywords: CreateTrackTerminal, CreateTrackTerminal method [TAPI 2.2], CreateTrackTerminal method [TAPI 2.2],ITMultiTrackTerminal interface, ITMultiTrackTerminal interface [TAPI 2.2],CreateTrackTerminal method, ITMultiTrackTerminal.CreateTrackTerminal, ITMultiTrackTerminal::CreateTrackTerminal, _tapi3_itmultitrackterminal_createtrackterminal, tapi3.itmultitrackterminal_createtrackterminal, tapi3if/ITMultiTrackTerminal::CreateTrackTerminal
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
 - ITMultiTrackTerminal::CreateTrackTerminal
 - tapi3if/ITMultiTrackTerminal::CreateTrackTerminal
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
 - ITMultiTrackTerminal.CreateTrackTerminal
---

# ITMultiTrackTerminal::CreateTrackTerminal


## -description

The 
<b>CreateTrackTerminal</b> method creates a multitrack terminal that can handle a given media type or types and media direction.

## -parameters

### -param MediaType [in]

Bitwise ORed list of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a> required for the terminal.

### -param TerminalDirection [in]

The 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">TERMINAL_DIRECTION</a> descriptor for the terminal.

### -param ppTerminal [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITMultiTrackTerminal::CreateTrackTerminal</b>. The application must call <b>Release</b> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal">ITMultiTrackTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>