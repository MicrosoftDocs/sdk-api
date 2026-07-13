---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetStreamSelection
title: IMFMediaEngineEx::SetStreamSelection (mfmediaengine.h)
description: Selects or deselects a stream for playback.
helpviewer_keywords: ["FALSE","IMFMediaEngineEx interface [Media Foundation]","SetStreamSelection method","IMFMediaEngineEx.SetStreamSelection","IMFMediaEngineEx::SetStreamSelection","SetStreamSelection","SetStreamSelection method [Media Foundation]","SetStreamSelection method [Media Foundation]","IMFMediaEngineEx interface","TRUE","mf.imfmediaengineex_setstreamselection","mfmediaengine/IMFMediaEngineEx::SetStreamSelection"]
old-location: mf\imfmediaengineex_setstreamselection.htm
tech.root: mf
ms.assetid: 12F0FDD0-0D8C-496D-B5C4-3FBCBCAAC6FB
ms.date: 12/05/2018
ms.keywords: FALSE, IMFMediaEngineEx interface [Media Foundation],SetStreamSelection method, IMFMediaEngineEx.SetStreamSelection, IMFMediaEngineEx::SetStreamSelection, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFMediaEngineEx interface, TRUE, mf.imfmediaengineex_setstreamselection, mfmediaengine/IMFMediaEngineEx::SetStreamSelection
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::SetStreamSelection
 - mfmediaengine/IMFMediaEngineEx::SetStreamSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.SetStreamSelection
---

# IMFMediaEngineEx::SetStreamSelection


## -description

Selects or deselects a stream for playback.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream. To get the number of streams, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getnumberofstreams">IMFMediaEngineEx::GetNumberOfStreams</a>.

### -param Enabled [in]

Specifies whether to select or deselect the stream.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The stream is selected. During playback, this stream will play.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The stream is not selected. During playback, this stream will not play.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>