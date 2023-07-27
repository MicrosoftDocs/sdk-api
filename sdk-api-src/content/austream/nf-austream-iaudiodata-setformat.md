---
UID: NF:austream.IAudioData.SetFormat
title: IAudioData::SetFormat (austream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetFormat method sets the current data format.
helpviewer_keywords: ["IAudioData interface [DirectShow]","SetFormat method","IAudioData.SetFormat","IAudioData::SetFormat","IAudioDataSetFormat","SetFormat","SetFormat method [DirectShow]","SetFormat method [DirectShow]","IAudioData interface","austream/IAudioData::SetFormat","dshow.iaudiodata_setformat"]
old-location: dshow\iaudiodata_setformat.htm
tech.root: dshow
ms.assetid: 792112a6-b10a-432f-854a-07bd74173e84
ms.date: 4/26/2023
ms.keywords: IAudioData interface [DirectShow],SetFormat method, IAudioData.SetFormat, IAudioData::SetFormat, IAudioDataSetFormat, SetFormat, SetFormat method [DirectShow], SetFormat method [DirectShow],IAudioData interface, austream/IAudioData::SetFormat, dshow.iaudiodata_setformat
req.header: austream.h
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
 - IAudioData::SetFormat
 - austream/IAudioData::SetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IAudioData.SetFormat
---

# IAudioData::SetFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetFormat</code> method sets the current data format.

## -parameters

### -param lpWaveFormat [in]

Pointer to a <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that will contain the current data format.

## -returns

Returns an <b>HRESULT</b> value, which can include the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid format.

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

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData Interface</a>



<a href="/windows/desktop/api/austream/nf-austream-iaudiodata-getformat">IAudioData::GetFormat</a>