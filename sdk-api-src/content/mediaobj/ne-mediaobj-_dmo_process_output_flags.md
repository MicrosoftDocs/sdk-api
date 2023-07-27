---
UID: NE:mediaobj._DMO_PROCESS_OUTPUT_FLAGS
title: "_DMO_PROCESS_OUTPUT_FLAGS (mediaobj.h)"
description: The DMO_PROCESS_OUTPUT_FLAGS enumeration defines flags that specify output processing requests.
helpviewer_keywords: ["DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER","DMO_PROCESS_OUTPUT_FLAGS","DMO_PROCESS_OUTPUT_FLAGSEnumeration","_DMO_PROCESS_OUTPUT_FLAGS","_DMO_PROCESS_OUTPUT_FLAGS enumeration [DirectShow]","dshow.dmo_process_output_flags","mediaobj/DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER","mediaobj/_DMO_PROCESS_OUTPUT_FLAGS"]
old-location: dshow\dmo_process_output_flags.htm
tech.root: dshow
ms.assetid: 7648f975-3753-41fe-a311-e86334ef7071
ms.date: 4/26/2023
ms.keywords: DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, DMO_PROCESS_OUTPUT_FLAGS , DMO_PROCESS_OUTPUT_FLAGSEnumeration, _DMO_PROCESS_OUTPUT_FLAGS, _DMO_PROCESS_OUTPUT_FLAGS enumeration [DirectShow], dshow.dmo_process_output_flags, mediaobj/DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER, mediaobj/_DMO_PROCESS_OUTPUT_FLAGS
req.header: mediaobj.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DMO_PROCESS_OUTPUT_FLAGS
 - mediaobj/_DMO_PROCESS_OUTPUT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_PROCESS_OUTPUT_FLAGS
---

# _DMO_PROCESS_OUTPUT_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DMO_PROCESS_OUTPUT_FLAGS</code> enumeration defines flags that specify output processing requests.

## -enum-fields

### -field DMO_PROCESS_OUTPUT_DISCARD_WHEN_NO_BUFFER:0x1

Discard the output when the pointer to the output buffer is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a>
