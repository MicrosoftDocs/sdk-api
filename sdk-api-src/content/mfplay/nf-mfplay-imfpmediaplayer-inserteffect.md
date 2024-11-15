---
UID: NF:mfplay.IMFPMediaPlayer.InsertEffect
title: IMFPMediaPlayer::InsertEffect (mfplay.h)
description: Applies an audio or video effect to playback.
helpviewer_keywords: ["FALSE","IMFPMediaPlayer interface [Media Foundation]","InsertEffect method","IMFPMediaPlayer.InsertEffect","IMFPMediaPlayer::InsertEffect","InsertEffect","InsertEffect method [Media Foundation]","InsertEffect method [Media Foundation]","IMFPMediaPlayer interface","TRUE","mf.imfpmediaplayer_inserteffect","mfplay/IMFPMediaPlayer::InsertEffect"]
old-location: mf\imfpmediaplayer_inserteffect.htm
tech.root: mfarchive
archived: true
ms.assetid: 2689ee46-5cfe-4616-850c-eb5aef340daa
ms.date: 12/05/2018
ms.keywords: FALSE, IMFPMediaPlayer interface [Media Foundation],InsertEffect method, IMFPMediaPlayer.InsertEffect, IMFPMediaPlayer::InsertEffect, InsertEffect, InsertEffect method [Media Foundation], InsertEffect method [Media Foundation],IMFPMediaPlayer interface, TRUE, mf.imfpmediaplayer_inserteffect, mfplay/IMFPMediaPlayer::InsertEffect
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
 - IMFPMediaPlayer::InsertEffect
 - mfplay/IMFPMediaPlayer::InsertEffect
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
 - IMFPMediaPlayer.InsertEffect
---

# IMFPMediaPlayer::InsertEffect


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Applies an audio or video effect to playback.

## -parameters

### -param pEffect [in]

Pointer to the <b>IUnknown</b> interface for one of the following: 

<ul>
<li>A Media Foundation transform (MFT) that implements the effect. MFTs expose the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.</li>
<li>An activation object that creates an MFT. Activation objects expose the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface.</li>
</ul>

### -param fOptional [in]

Specifies whether the effect is optional.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The effect is optional. If the MFPlay player object cannot add the effect, it ignores the effect and  continues playback.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
If the MFPlay player object cannot add the effect, a playback error occurs.

</td>
</tr>
</table>

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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDINDEX</b></b></dt>
</dl>
</td>
<td width="60%">
This effect was already added.

</td>
</tr>
</table>

## -remarks

The object specified in the <i>pEffect</i> parameter can implement either a video effect or an audio effect. The effect is applied to any media items set after the method is called. It is not applied to the current media item. 

For each media item, the effect is applied to the first selected stream of the matching type (audio or video). If a media item has two selected streams of the same type, the second stream does not receive the effect. The effect is ignored if the media item does not contain a stream that matches the effect type. For example, if you set a video effect and play a file that contains just audio, the video effect is ignored, although no error is raised.

The effect is applied to all subsequent media items, until the application removes the effect. To remove an effect, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect">IMFPMediaPlayer::RemoveEffect</a> or <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects">IMFPMediaPlayer::RemoveAllEffects</a>.

If you set multiple effects of the same type (audio or video), they are applied in the same order in which you call <b>InsertEffect</b>.

<h3><a id="Remote_Playback_Optimizations"></a><a id="remote_playback_optimizations"></a><a id="REMOTE_PLAYBACK_OPTIMIZATIONS"></a>Remote Playback Optimizations</h3>
Audio and video effects might be incompatible with optimizations that are used for remote playback. The following remarks apply only to audio or video effects that are actually used during playback:

<ul>
<li>If you mark an audio or video effect as required, by setting <i>fOptional</i> to <b>FALSE</b>, MFPlay disables remote playback optimizations.</li>
<li>Otherwise, if all audio/video effects are marked as optional, MFPlay  might drop the effects, in order to enable remote playback optimizations.</li>
</ul>
In other words, required effects have priority over remote optimizations, but optional effects do not.

Remote optimizations might be disabled for other reasons. For example, they are disabled if you set the <b>MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION</b> option when you create the player object. In that case, MFPlay will attempt to insert any optional effects. 

Non-audio, non-video effects do not affect remote optimizations. Also, if you insert a required effect but the source does not contain any streams of that type, remote optimizations are not disabled.


#### Examples


```cpp
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/how-to-add-audio-or-video-effects">How to Add Audio or Video Effects</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>