---
UID: NF:tapi3if.ITMultiTrackTerminal.get_MediaTypesInUse
title: ITMultiTrackTerminal::get_MediaTypesInUse (tapi3if.h)
description: The get_MediaTypesInUse method returns the media types (bitwise ORed) of all tracks managed currently by the multitrack terminal.
helpviewer_keywords: ["ITMultiTrackTerminal interface [TAPI 2.2]","get_MediaTypesInUse method","ITMultiTrackTerminal.get_MediaTypesInUse","ITMultiTrackTerminal::get_MediaTypesInUse","_tapi3_itmultitrackterminal_get_mediatypesinuse","get_MediaTypesInUse","get_MediaTypesInUse method [TAPI 2.2]","get_MediaTypesInUse method [TAPI 2.2]","ITMultiTrackTerminal interface","tapi3.itmultitrackterminal_get_mediatypesinuse","tapi3if/ITMultiTrackTerminal::get_MediaTypesInUse"]
old-location: tapi3\itmultitrackterminal_get_mediatypesinuse.htm
tech.root: tapi3
ms.assetid: 0c2ebbba-66a4-4ef0-abba-faab129e64e2
ms.date: 12/05/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],get_MediaTypesInUse method, ITMultiTrackTerminal.get_MediaTypesInUse, ITMultiTrackTerminal::get_MediaTypesInUse, _tapi3_itmultitrackterminal_get_mediatypesinuse, get_MediaTypesInUse, get_MediaTypesInUse method [TAPI 2.2], get_MediaTypesInUse method [TAPI 2.2],ITMultiTrackTerminal interface, tapi3.itmultitrackterminal_get_mediatypesinuse, tapi3if/ITMultiTrackTerminal::get_MediaTypesInUse
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
 - ITMultiTrackTerminal::get_MediaTypesInUse
 - tapi3if/ITMultiTrackTerminal::get_MediaTypesInUse
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
 - ITMultiTrackTerminal.get_MediaTypesInUse
---

# ITMultiTrackTerminal::get_MediaTypesInUse


## -description

The 
<b>get_MediaTypesInUse</b> method returns the media types (bitwise ORed) of all tracks managed currently by the multitrack terminal. For tracks that are multitrack terminals themselves, this method calls the track's <b>ITMultiTrackTerminal::get_MediaTypesInUse</b> method to determine the track's media types.

## -parameters

### -param plMediaTypesInUse [out]

Bitwise ORed list of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media types</a> in use.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal">ITMultiTrackTerminal</a>