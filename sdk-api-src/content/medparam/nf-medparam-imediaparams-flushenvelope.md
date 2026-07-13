---
UID: NF:medparam.IMediaParams.FlushEnvelope
title: IMediaParams::FlushEnvelope (medparam.h)
description: The FlushEnvelope method flushes envelope data for a specified parameter over the specified time range.
helpviewer_keywords: ["FlushEnvelope","FlushEnvelope method [DirectShow]","FlushEnvelope method [DirectShow]","IMediaParams interface","IMediaParams interface [DirectShow]","FlushEnvelope method","IMediaParams.FlushEnvelope","IMediaParams::FlushEnvelope","IMediaParamsFlushEnvelope","dshow.imediaparams_flushenvelope","medparam/IMediaParams::FlushEnvelope"]
old-location: dshow\imediaparams_flushenvelope.htm
tech.root: dshow
ms.assetid: 574d6573-ea5d-4419-ad65-f5f7d711e720
ms.date: 4/26/2023
ms.keywords: FlushEnvelope, FlushEnvelope method [DirectShow], FlushEnvelope method [DirectShow],IMediaParams interface, IMediaParams interface [DirectShow],FlushEnvelope method, IMediaParams.FlushEnvelope, IMediaParams::FlushEnvelope, IMediaParamsFlushEnvelope, dshow.imediaparams_flushenvelope, medparam/IMediaParams::FlushEnvelope
req.header: medparam.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaParams::FlushEnvelope
 - medparam/IMediaParams::FlushEnvelope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParams.FlushEnvelope
---

# IMediaParams::FlushEnvelope


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>FlushEnvelope</code> method flushes envelope data for a specified parameter over the specified time range.

## -parameters

### -param dwParamIndex [in]

Zero-based index of the parameter, or DWORD_ALLPARAMS to flush envelope data from every parameter.

### -param refTimeStart [in]

Start time of the envelope data to flush.

### -param refTimeEnd [in]

Stop time of the envelope data to flush.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

If the time span specified by <i>refTimeStart</i> and <i>refTimeEnd</i> overlaps an envelope segment, the entire segment is flushed. On the other hand, if it falls on the boundary of an envelope segment, the entire segment is retained. Thus:

<ul>
<li>If the start time falls inside an envelope segment, the segment is flushed.</li>
<li>If the end time falls inside an envelope segment, the segment is flushed.</li>
<li>If the start time equals the end time of an envelope segment, the segment is retained.</li>
<li>If the end time equals the start time of an envelope segment, the segment is retained.</li>
</ul>
To enumerate the parameters supported by this object, along with their index values, use the <a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo</a> interface.

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams Interface</a>