---
UID: NF:mfplay.IMFPMediaItem.GetDuration
title: IMFPMediaItem::GetDuration (mfplay.h)
description: Gets the duration of the media item.
helpviewer_keywords: ["GetDuration","GetDuration method [Media Foundation]","GetDuration method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetDuration method","IMFPMediaItem.GetDuration","IMFPMediaItem::GetDuration","MFP_POSITIONTYPE_100NS","mf.imfpmediaitem_getduration","mfplay/IMFPMediaItem::GetDuration"]
old-location: mf\imfpmediaitem_getduration.htm
tech.root: mfarchive
archived: true
ms.assetid: 831f023b-c06f-4099-9f4c-df38f3d1382f
ms.date: 12/05/2018
ms.keywords: GetDuration, GetDuration method [Media Foundation], GetDuration method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetDuration method, IMFPMediaItem.GetDuration, IMFPMediaItem::GetDuration, MFP_POSITIONTYPE_100NS, mf.imfpmediaitem_getduration, mfplay/IMFPMediaItem::GetDuration
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
 - IMFPMediaItem::GetDuration
 - mfplay/IMFPMediaItem::GetDuration
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
 - IMFPMediaItem.GetDuration
---

# IMFPMediaItem::GetDuration


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the duration of the media item.

## -parameters

### -param guidPositionType [in]

Specifies the unit of time for the duration value. The following value is defined.

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
               

The value returned in <i>pvDurationValue</i> is a <b>LARGE_INTEGER</b>.

<ul>
<li>Variant type (<b>vt</b>): VT_I8</li>
<li>Variant member: <b>hVal</b></li>
</ul>
</td>
</tr>
</table>

### -param pvDurationValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the duration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The method returns the total duration of the content, regardless of any values set through <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition">IMFPMediaItem::SetStartStopPosition</a>.


#### Examples


```cpp
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/how-to-get-the-playback-duration">How to Get the Playback Duration</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>