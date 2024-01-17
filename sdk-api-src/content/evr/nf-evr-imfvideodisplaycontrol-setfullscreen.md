---
UID: NF:evr.IMFVideoDisplayControl.SetFullscreen
title: IMFVideoDisplayControl::SetFullscreen (evr.h)
description: Sets or unsets full-screen rendering mode.
helpviewer_keywords: ["95c85fb2-9267-477f-aa47-1c050ccc1bdd","IMFVideoDisplayControl interface [Media Foundation]","SetFullscreen method","IMFVideoDisplayControl.SetFullscreen","IMFVideoDisplayControl::SetFullscreen","SetFullscreen","SetFullscreen method [Media Foundation]","SetFullscreen method [Media Foundation]","IMFVideoDisplayControl interface","evr/IMFVideoDisplayControl::SetFullscreen","mf.imfvideodisplaycontrol_setfullscreen"]
old-location: mf\imfvideodisplaycontrol_setfullscreen.htm
tech.root: mfarchive
ms.assetid: 95c85fb2-9267-477f-aa47-1c050ccc1bdd
ms.date: 12/05/2018
ms.keywords: 95c85fb2-9267-477f-aa47-1c050ccc1bdd, IMFVideoDisplayControl interface [Media Foundation],SetFullscreen method, IMFVideoDisplayControl.SetFullscreen, IMFVideoDisplayControl::SetFullscreen, SetFullscreen, SetFullscreen method [Media Foundation], SetFullscreen method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetFullscreen, mf.imfvideodisplaycontrol_setfullscreen
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFVideoDisplayControl::SetFullscreen
 - evr/IMFVideoDisplayControl::SetFullscreen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.SetFullscreen
archived: true
---

# IMFVideoDisplayControl::SetFullscreen


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. ]

Sets or unsets full-screen rendering mode.

To implement full-screen playback, an application should simply resize the video window to cover the entire area of the monitor. Also set the window to be a topmost window, so that the application receives all mouse-click messages. For more information about topmost windows, see the documentation for the <a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a> function.

## -parameters

### -param fFullscreen [in]

If <b>TRUE</b>, the enhanced video renderer (EVR) uses full-screen mode. If <b>FALSE</b>, the EVR draws the video in the application-provided clipping window.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.
              

</td>
</tr>
</table>

## -remarks

The default EVR presenter implements full-screen mode using Direct3D exclusive mode.
      

If you use this  method  to switch to full-screen mode, set the application window to be a topmost window and resize the window to cover the entire monitor. This ensures that the application window receives all mouse-click messages. Also set the keyboard focus to the application window. When you switch out of full-screen mode, restore the window's original size and position.
      

By default, the cursor is still visible in full-screen mode. To hide the cursor, call <b>ShowCursor</b>.
      

The transition to and from full-screen mode occurs asynchronously. To get the current mode, call <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getfullscreen">IMFVideoDisplayControl::GetFullscreen</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>