---
UID: NF:control.IAMStats.Reset
title: IAMStats::Reset (control.h)
description: The Reset method resets all statistics to zero.
helpviewer_keywords: ["IAMStats interface [DirectShow]","Reset method","IAMStats.Reset","IAMStats::Reset","IAMStatsReset","Reset","Reset method [DirectShow]","Reset method [DirectShow]","IAMStats interface","control/IAMStats::Reset","dshow.iamstats_reset"]
old-location: dshow\iamstats_reset.htm
tech.root: dshow
ms.assetid: daa5f3c0-6785-46b6-987f-acef798b0ed9
ms.date: 4/26/2023
ms.keywords: IAMStats interface [DirectShow],Reset method, IAMStats.Reset, IAMStats::Reset, IAMStatsReset, Reset, Reset method [DirectShow], Reset method [DirectShow],IAMStats interface, control/IAMStats::Reset, dshow.iamstats_reset
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMStats::Reset
 - control/IAMStats::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStats.Reset
---

# IAMStats::Reset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reset</code> method resets all statistics to zero.



## -returns

Returns S_OK if successful, or an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-iamstats">IAMStats Interface</a>
