---
UID: NF:mfplay.IMFPMediaPlayer.GetPosition
title: IMFPMediaPlayer::GetPosition (mfplay.h)
description: Gets the current playback position. (IMFPMediaPlayer.GetPosition)
helpviewer_keywords: ["GetPosition","GetPosition method [Media Foundation]","GetPosition method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetPosition method","IMFPMediaPlayer.GetPosition","IMFPMediaPlayer::GetPosition","MFP_POSITIONTYPE_100NS","mf.imfpmediaplayer_getposition","mfplay/IMFPMediaPlayer::GetPosition"]
old-location: mf\imfpmediaplayer_getposition.htm
tech.root: mfarchive
archived: true
ms.assetid: e3401c66-0dc7-46ef-9a38-088d605a3038
ms.date: 12/05/2018
ms.keywords: GetPosition, GetPosition method [Media Foundation], GetPosition method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetPosition method, IMFPMediaPlayer.GetPosition, IMFPMediaPlayer::GetPosition, MFP_POSITIONTYPE_100NS, mf.imfpmediaplayer_getposition, mfplay/IMFPMediaPlayer::GetPosition
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
 - IMFPMediaPlayer::GetPosition
 - mfplay/IMFPMediaPlayer::GetPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayer.GetPosition
---

# IMFPMediaPlayer::GetPosition


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the current playback position.

## -parameters

### -param guidPositionType [in]

Specifies the unit of time for the playback position. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFP_POSITIONTYPE_100NS"></a><a id="mfp_positiontype_100ns"></a><dl>
<dt><b>MFP_POSITIONTYPE_100NS</b></dt>
</dl>
</td>
<td width="60%">
100-nanosecond units. 

The value returned in <i>pvPositionValue</i> is a <b>LARGE_INTEGER</b>.

<ul>
<li>Variant type (<b>vt</b>): <b>VT_I8</b></li>
<li>Variant member: <b>hVal</b></li>
</ul>
</td>
</tr>
</table>

### -param pvPositionValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the playback position.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
No media item has been queued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

The playback position is calculated relative to the start time of the media item, which can be specified by calling <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition">IMFPMediaItem::SetStartStopPosition</a>. For example, if you set the start time to 20 seconds and the source duration is 60 seconds, the range of values returned by <b>GetPosition</b> is 0–40 seconds.


#### Examples

The following code gets the current position, in 100-nanosecond units, as a <b>LONGLONG</b> value.


```
HRESULT GetPositionHNS(
    IMFPMediaPlayer *pPlayer, 
    LONGLONG *phnsPosition    // Receives the position in hns.
)
{
    HRESULT hr = S_OK;

    PROPVARIANT var;
    PropVariantInit(&var);

    *phnsPosition = 0;

    hr = pPlayer->GetPosition(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        *phnsPosition = var.hVal.QuadPart;
    }

    PropVariantClear(&var);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
