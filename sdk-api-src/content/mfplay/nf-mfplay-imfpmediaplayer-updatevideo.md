---
UID: NF:mfplay.IMFPMediaPlayer.UpdateVideo
title: IMFPMediaPlayer::UpdateVideo
author: windows-sdk-content
description: Updates the video frame.
old-location: mf\imfpmediaplayer_updatevideo.htm
tech.root: MedFound
ms.assetid: de583e74-b31b-407e-af4b-c36649e1ca84
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],UpdateVideo method, IMFPMediaPlayer.UpdateVideo, IMFPMediaPlayer::UpdateVideo, UpdateVideo, UpdateVideo method [Media Foundation], UpdateVideo method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_updatevideo, mfplay/IMFPMediaPlayer::UpdateVideo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayer.UpdateVideo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMediaPlayer::UpdateVideo


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Updates the video frame.


## -parameters






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
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
The current media item does not contain video.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="https://msdn.microsoft.com/c56b07b5-f595-4933-9af6-868fc8938849">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



Call this method when your application's video playback window receives either a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> or <a href="https://msdn.microsoft.com/en-us/library/ms632646(v=VS.85).aspx">WM_SIZE</a> message. This method performs two functions:
        
        

<ul>
<li>Ensures that the video frame is repainted while playback is paused or stopped.  </li>
<li>Adjusts the displayed video to match the current size of the video window.</li>
</ul>
<div class="alert"><b>Important</b>  Call the GDI <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function before calling  <b>UpdateVideo</b>.</div>
<div> </div>

#### Examples

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IMFPMediaPlayer *g_pPlayer;

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    HDC hdc;
    PAINTSTRUCT ps;

    switch (uMsg)
    {
    case WM_PAINT:
        hdc = BeginPaint(hwnd, &amp;ps);
        if (g_pPlayer)
        {
            g_pPlayer-&gt;UpdateVideo();
        }
       	EndPaint(hwnd, &amp;ps);
        break;

    case WM_SIZE:        
        hdc = BeginPaint(hwnd, &amp;ps);
        if (g_pPlayer)
        {
            g_pPlayer-&gt;UpdateVideo();
        }
       	EndPaint(hwnd, &amp;ps);
        break;

    // other messages

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    }
    return 0;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

