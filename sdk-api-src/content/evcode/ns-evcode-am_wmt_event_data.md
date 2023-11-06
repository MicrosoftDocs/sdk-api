---
UID: NS:evcode.AM_WMT_EVENT_DATA
title: AM_WMT_EVENT_DATA (evcode.h)
description: The AM_WMT_EVENT_DATA structure contains information pertaining to an EC_WMT_EVENT and the associated status code returned by the Windows Media Format SDK.
helpviewer_keywords: ["AM_WMT_EVENT_DATA","AM_WMT_EVENT_DATA structure [windows Media Format]","evcode/AM_WMT_EVENT_DATA","wmformat.am_wmt_event_data"]
old-location: wmformat\am_wmt_event_data.htm
tech.root: wmformat
ms.assetid: 49f48cb6-e1d0-4dd4-bfb4-c5917144c3cf
ms.date: 4/26/2023
ms.keywords: AM_WMT_EVENT_DATA, AM_WMT_EVENT_DATA structure [windows Media Format], evcode/AM_WMT_EVENT_DATA, wmformat.am_wmt_event_data
req.header: evcode.h
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
req.typenames: AM_WMT_EVENT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_WMT_EVENT_DATA
 - evcode/AM_WMT_EVENT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcode.h
api_name:
 - AM_WMT_EVENT_DATA
---

# AM_WMT_EVENT_DATA structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AM_WMT_EVENT_DATA</b> structure contains information pertaining to an <a href="/windows/desktop/wmformat/ec-wmt-event">EC_WMT_EVENT</a> and the associated status code returned by the Windows Media Format SDK.

## -struct-fields

### -field hrStatus

The status code returned by the Windows Media Format SDK.

### -field pData

Pointer whose data is dependent on the value of the <b>WMT_STATUS</b> message in <i>lParam1</i> of the <b>EC_WMT_EVENT</b> event. For more information, see <a href="/windows/desktop/wmformat/ec-wmt-event">EC_WMT_EVENT</a>.

## -remarks

This structure is relevant when using the <a href="/windows/desktop/wmformat/wm-asf-reader-filter">WM ASF Reader</a> filter to read files protected with Digital Rights Management.

