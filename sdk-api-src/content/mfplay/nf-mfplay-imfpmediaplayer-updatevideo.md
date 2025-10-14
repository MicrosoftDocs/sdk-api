---
UID: NF:mfplay.IMFPMediaPlayer.UpdateVideo
title: IMFPMediaPlayer::UpdateVideo (mfplay.h)
description: Updates the video frame. (IMFPMediaPlayer.UpdateVideo)
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","UpdateVideo method","IMFPMediaPlayer.UpdateVideo","IMFPMediaPlayer::UpdateVideo","UpdateVideo","UpdateVideo method [Media Foundation]","UpdateVideo method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_updatevideo","mfplay/IMFPMediaPlayer::UpdateVideo"]
old-location: mf\imfpmediaplayer_updatevideo.htm
tech.root: mfarchive
archived: true
ms.assetid: de583e74-b31b-407e-af4b-c36649e1ca84
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],UpdateVideo method, IMFPMediaPlayer.UpdateVideo, IMFPMediaPlayer::UpdateVideo, UpdateVideo, UpdateVideo method [Media Foundation], UpdateVideo method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_updatevideo, mfplay/IMFPMediaPlayer::UpdateVideo
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
 - IMFPMediaPlayer::UpdateVideo
 - mfplay/IMFPMediaPlayer::UpdateVideo
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
 - IMFPMediaPlayer.UpdateVideo
---

# IMFPMediaPlayer::UpdateVideo


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Updates the video frame.



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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The current media item does not contain video.

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

Call this method when your application's video playback window receives either a <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> or <a href="/windows/desktop/winmsg/wm-size">WM_SIZE</a> message. This method performs two functions:
        
        

<ul>
<li>Ensures that the video frame is repainted while playback is paused or stopped.  </li>
<li>Adjusts the displayed video to match the current size of the video window.</li>
</ul>
<div class="alert"><b>Important</b>  Call the GDI <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function before calling  <b>UpdateVideo</b>.</div>
<div> </div>

#### Examples


```
IMFPMediaPlayer *g_pPlayer;

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    HDC hdc;
    PAINTSTRUCT ps;

    switch (uMsg)
    {
    case WM_PAINT:
        hdc = BeginPaint(hwnd, &ps);
        if (g_pPlayer)
        {
            g_pPlayer->UpdateVideo();
        }
       	EndPaint(hwnd, &ps);
        break;

    case WM_SIZE:        
        hdc = BeginPaint(hwnd, &ps);
        if (g_pPlayer)
        {
            g_pPlayer->UpdateVideo();
        }
       	EndPaint(hwnd, &ps);
        break;

    // other messages

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    }
    return 0;
}
```

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
