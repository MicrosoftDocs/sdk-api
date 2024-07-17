---
UID: NF:mfplay.MFP_GET_POSITION_SET_EVENT
title: MFP_GET_POSITION_SET_EVENT macro (mfplay.h)
description: Casts an MFP_EVENT_HEADER pointer to an MFP_POSITION_SET_EVENT pointer.
helpviewer_keywords: ["MFP_GET_POSITION_SET_EVENT","MFP_GET_POSITION_SET_EVENT macro [Media Foundation]","mf.mfp_get_position_set_event","mfplay/MFP_GET_POSITION_SET_EVENT"]
old-location: mf\mfp_get_position_set_event.htm
tech.root: mfarchive
archived: true
ms.assetid: e9b692e6-7b7c-45ac-bbaa-7060578f9403
ms.date: 12/05/2018
ms.keywords: MFP_GET_POSITION_SET_EVENT, MFP_GET_POSITION_SET_EVENT macro [Media Foundation], mf.mfp_get_position_set_event, mfplay/MFP_GET_POSITION_SET_EVENT
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_GET_POSITION_SET_EVENT
 - mfplay/MFP_GET_POSITION_SET_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_GET_POSITION_SET_EVENT
---

# MFP_GET_POSITION_SET_EVENT macro


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Casts an <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> pointer to an <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_position_set_event">MFP_POSITION_SET_EVENT</a> pointer.

## -parameters

### -param pHdr

Pointer to an <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure.

## -remarks

The <b>eEventType</b> member of the input structure must be <b>MFP_EVENT_TYPE_POSITION_SET</b>. Otherwise, the macro returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-macros">Media Foundation Macros</a>