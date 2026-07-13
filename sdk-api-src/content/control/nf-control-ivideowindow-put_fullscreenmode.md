---
UID: NF:control.IVideoWindow.put_FullScreenMode
title: IVideoWindow::put_FullScreenMode (control.h)
description: The put_FullScreenMode method enables or disables full-screen video rendering.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_FullScreenMode method","IVideoWindow.put_FullScreenMode","IVideoWindow::put_FullScreenMode","IVideoWindowput_FullScreenMode","control/IVideoWindow::put_FullScreenMode","dshow.ivideowindow_put_fullscreenmode","put_FullScreenMode","put_FullScreenMode method [DirectShow]","put_FullScreenMode method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_fullscreenmode.htm
tech.root: dshow
ms.assetid: efa1c6ed-bea5-4c25-89c2-1b6fcdad3834
ms.date: 4/26/2023
ms.keywords: IVideoWindow interface [DirectShow],put_FullScreenMode method, IVideoWindow.put_FullScreenMode, IVideoWindow::put_FullScreenMode, IVideoWindowput_FullScreenMode, control/IVideoWindow::put_FullScreenMode, dshow.ivideowindow_put_fullscreenmode, put_FullScreenMode, put_FullScreenMode method [DirectShow], put_FullScreenMode method [DirectShow],IVideoWindow interface
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IVideoWindow::put_FullScreenMode
 - control/IVideoWindow::put_FullScreenMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.put_FullScreenMode
---

# IVideoWindow::put_FullScreenMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_FullScreenMode</code> method enables or disables full-screen video rendering.

## -parameters

### -param FullScreenMode [in]

Boolean value that specifies whether to enable or disable full-screen mode. Must be one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE
                </td>
<td>Switch to full-screen mode.</td>
</tr>
<tr>
<td>OAFALSE
                </td>
<td>Disable full-screen mode. (Default.)</td>
</tr>
</table>

## -returns

Possible return values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Filter does not support full-screen mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Already in the requested mode.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_FULLSCREEN</b></dt>
</dl>
</td>
<td width="60%">
Could not find any filter that supports full-screen mode.

</td>
</tr>
</table>

## -remarks

Depending on the video renderer, the switch to full-screen mode may not be visible until the application runs or pauses the graph. In full-screen mode, if the user switches away from the application (for example, using ALT + TAB), the Filter Graph Manager sends an <a href="/windows/desktop/DirectShow/ec-fullscreen-lost">EC_FULLSCREEN_LOST</a> event.

The following remarks describe how the Filter Graph Manager implements full-screen mode. Application developers can probably ignore this information, but it may be useful if you are writing a custom video renderer.

When an application switches to full-screen mode, the Filter Graph Manager searches for a video renderer that will function most efficiently. In order of preference, these are:

<ol>
<li>Any video renderer in the filter graph that natively supports full-screen mode.</li>
<li>Any video renderer in the filter graph that can stretch the video to full-screen without a significant performance cost.</li>
<li>The <a href="/windows/desktop/DirectShow/full-screen-renderer-filter">Full Screen Renderer</a> filter.</li>
<li>Any video renderer in the filter graph that supports <b>IVideoWindow</b>.</li>
</ol>
For the first option, the Filter Graph Manager calls <a href="/windows/desktop/api/control/nf-control-ivideowindow-get_fullscreenmode">IVideoWindow::get_FullScreenMode</a> on every video renderer in the graph. Most renderers return E_NOTIMPL, indicating the filter does not natively support full-screen mode. If any renderer returns a value not equal to E_NOTIMPL, the Filter Graph Manager uses that one.

For the second option, the Filter Graph Manager calls <a href="/windows/desktop/api/control/nf-control-ivideowindow-getmaxidealimagesize">IVideoWindow::GetMaxIdealImageSize</a> and <b>GetMinIdealImageSize</b> on every video renderer in the graph. If the size of the display falls within the filter's reported range, it indicates that the filter can stretch the video without a significant performance cost.

<div class="alert"><b>Note</b>  If the graph is stopped, the Filter Graph Manager pauses each renderer before calling these methods. This gives the renderer an opportunity to initialize any resources it needs, because many renderers cannot determine these values while they are stopped.</div>
<div> </div>
Except on older hardware, the second option will generally succeed. The third option is to use the Full Screen Renderer filter, adding it to the graph if necessary. The fourth option is simply to find the first renderer in the graph that supports <b>IVideoWindow</b>, and stretch the video regardless of performance.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_fullscreenmode">IVideoWindow::get_FullScreenMode</a>