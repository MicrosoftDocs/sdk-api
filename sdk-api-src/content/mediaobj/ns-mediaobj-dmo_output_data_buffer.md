---
UID: NS:mediaobj._DMO_OUTPUT_DATA_BUFFER
title: DMO_OUTPUT_DATA_BUFFER (mediaobj.h)
description: The DMO_OUTPUT_DATA_BUFFER structure describes an output buffer used by a Microsoft DirectX Media Object (DMO).
helpviewer_keywords: ["*PDMO_OUTPUT_DATA_BUFFER","DMO_OUTPUT_DATA_BUFFER","DMO_OUTPUT_DATA_BUFFER structure [DirectShow]","DMO_OUTPUT_DATA_BUFFERStructure","PDMO_OUTPUT_DATA_BUFFER","PDMO_OUTPUT_DATA_BUFFER structure pointer [DirectShow]","dshow.dmo_output_data_buffer","mediaobj/DMO_OUTPUT_DATA_BUFFER","mediaobj/PDMO_OUTPUT_DATA_BUFFER"]
old-location: dshow\dmo_output_data_buffer.htm
tech.root: dshow
ms.assetid: 87fa2000-8dab-4f30-940a-14fb6699f616
ms.date: 4/26/2023
ms.keywords: '*PDMO_OUTPUT_DATA_BUFFER, DMO_OUTPUT_DATA_BUFFER, DMO_OUTPUT_DATA_BUFFER structure [DirectShow], DMO_OUTPUT_DATA_BUFFERStructure, PDMO_OUTPUT_DATA_BUFFER, PDMO_OUTPUT_DATA_BUFFER structure pointer [DirectShow], dshow.dmo_output_data_buffer, mediaobj/DMO_OUTPUT_DATA_BUFFER, mediaobj/PDMO_OUTPUT_DATA_BUFFER'
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
req.typenames: DMO_OUTPUT_DATA_BUFFER, *PDMO_OUTPUT_DATA_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DMO_OUTPUT_DATA_BUFFER
 - mediaobj/_DMO_OUTPUT_DATA_BUFFER
 - PDMO_OUTPUT_DATA_BUFFER
 - mediaobj/PDMO_OUTPUT_DATA_BUFFER
 - DMO_OUTPUT_DATA_BUFFER
 - mediaobj/DMO_OUTPUT_DATA_BUFFER
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
 - DMO_OUTPUT_DATA_BUFFER
---

# DMO_OUTPUT_DATA_BUFFER structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DMO_OUTPUT_DATA_BUFFER</code> structure describes an output buffer used by a Microsoft DirectX Media Object (DMO).

## -struct-fields

### -field pBuffer

Pointer to the <a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer</a> interface of a buffer allocated by the application.

### -field dwStatus

Status flags. After processing output, the DMO sets this member to a bitwise combination of zero or more <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_output_data_buffer_flags">DMO_OUTPUT_DATA_BUFFER_FLAGS</a> flags.

### -field rtTimestamp

Time stamp that specifies the start time of the data in the buffer. If the buffer has a valid time stamp, the DMO sets this member and also sets the DMO_OUTPUT_DATA_BUFFERF_TIME flag in the <b>dwStatus</b> member. Otherwise, ignore this member.

### -field rtTimelength

Reference time specifying the length of the data in the buffer. If the DMO sets this member to a valid value, it also sets the DMO_OUTPUT_DATA_BUFFERF_TIMELENGTH flag in the <b>dwStatus</b> member. Otherwise, ignore this member.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-structures">DMO Structures</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a>