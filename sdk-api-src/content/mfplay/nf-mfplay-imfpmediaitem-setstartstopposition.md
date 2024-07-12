---
UID: NF:mfplay.IMFPMediaItem.SetStartStopPosition
title: IMFPMediaItem::SetStartStopPosition (mfplay.h)
description: Sets the start and stop time for the media item.
helpviewer_keywords: ["IMFPMediaItem interface [Media Foundation]","SetStartStopPosition method","IMFPMediaItem.SetStartStopPosition","IMFPMediaItem::SetStartStopPosition","SetStartStopPosition","SetStartStopPosition method [Media Foundation]","SetStartStopPosition method [Media Foundation]","IMFPMediaItem interface","mf.imfpmediaitem_setstartstopposition","mfplay/IMFPMediaItem::SetStartStopPosition"]
old-location: mf\imfpmediaitem_setstartstopposition.htm
tech.root: mfarchive
archived: true
ms.assetid: 8f0409a6-1911-47ee-ac65-68b87d6b1db5
ms.date: 12/05/2018
ms.keywords: IMFPMediaItem interface [Media Foundation],SetStartStopPosition method, IMFPMediaItem.SetStartStopPosition, IMFPMediaItem::SetStartStopPosition, SetStartStopPosition, SetStartStopPosition method [Media Foundation], SetStartStopPosition method [Media Foundation],IMFPMediaItem interface, mf.imfpmediaitem_setstartstopposition, mfplay/IMFPMediaItem::SetStartStopPosition
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
 - IMFPMediaItem::SetStartStopPosition
 - mfplay/IMFPMediaItem::SetStartStopPosition
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
 - IMFPMediaItem.SetStartStopPosition
---

# IMFPMediaItem::SetStartStopPosition


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Sets the start and stop time for the media item.

## -parameters

### -param pguidStartPositionType [in]

Unit of time for the start position. See Remarks. This parameter can be <b>NULL</b>.

### -param pvStartValue [in]

Start position. The meaning and data type of this parameter are indicated by the <i>pguidStartPositionType</i> parameter. The  <i>pvStartValue</i> parameter must be <b>NULL</b> if <i>pguidStartPositionType</i> is <b>NULL</b>, and cannot be <b>NULL</b> otherwise.

### -param pguidStopPositionType [in]

Unit of time for the stop position. See Remarks. This parameter can be <b>NULL</b>.

### -param pvStopValue [in]

Stop position. The meaning and data type of this parameter are indicated by the <i>pguidStopPositionType</i> parameter. The <i>pvStopValue</i>  parameter must be <b>NULL</b> if <i>pguidStopPositionType</i> is <b>NULL</b>, and cannot be <b>NULL</b> otherwise.

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
<dt><b>MF_E_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Invalid start or stop time. Any of the following can cause this error:

<ul>
<li>Time less than zero.</li>
<li>Time greater than the total duration of the media item.</li>
<li>Stop time less than start time.</li>
</ul>
</td>
</tr>
</table>

## -remarks

By default, a media item plays from the beginning to the end of the file. This method adjusts the start time and/or  the stop time:

<ul>
<li>To set the start time, pass non-<b>NULL</b> values for <i>pguidStartPositionType</i> and <i>pvStartValue</i>.</li>
<li>To set the stop time, pass non-<b>NULL</b> values for <i>pguidStopPositionType</i> and <i>pvStopValue</i>.</li>
</ul>
The <i>pguidStartPositionType</i> and <i>pguidStopPositionType</i> parameters give the units of time that are used. Currently, the only supported value is <b>MFP_POSITIONTYPE_100NS</b>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>MFP_POSITIONTYPE_100NS</b></td>
<td>100-nanosecond units. The time parameter (<i>pvStartValue</i> or <i>pvStopValue</i>) uses the following data type:<ul>
<li>Variant type (<b>vt</b>): <b>VT_I8</b></li>
<li>Variant member: <b>hVal</b></li>
</ul>
To clear a previously set time, use an empty <b>PROPVARIANT</b> (<b>VT_EMPTY</b>).

</td>
</tr>
</table>
 

The adjusted start and stop times are used the next time that <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a> is called with this media item. If the media item is already set on the player, the change does not happen unless you call <b>SetMediaItem</b> again.


#### Examples


```cpp
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/how-to-play-a-file-clip">How to Play a File Clip</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>