---
UID: NF:evr.IMFVideoDisplayControl.SetVideoPosition
title: IMFVideoDisplayControl::SetVideoPosition (evr.h)
description: Sets the source and destination rectangles for the video.
helpviewer_keywords: ["5dc789b7-e206-4f1d-a0b2-12cb98ce4184","IMFVideoDisplayControl interface [Media Foundation]","SetVideoPosition method","IMFVideoDisplayControl.SetVideoPosition","IMFVideoDisplayControl::SetVideoPosition","SetVideoPosition","SetVideoPosition method [Media Foundation]","SetVideoPosition method [Media Foundation]","IMFVideoDisplayControl interface","evr/IMFVideoDisplayControl::SetVideoPosition","mf.imfvideodisplaycontrol_setvideoposition"]
old-location: mf\imfvideodisplaycontrol_setvideoposition.htm
tech.root: mfarchive
ms.assetid: 5dc789b7-e206-4f1d-a0b2-12cb98ce4184
ms.date: 12/05/2018
ms.keywords: 5dc789b7-e206-4f1d-a0b2-12cb98ce4184, IMFVideoDisplayControl interface [Media Foundation],SetVideoPosition method, IMFVideoDisplayControl.SetVideoPosition, IMFVideoDisplayControl::SetVideoPosition, SetVideoPosition, SetVideoPosition method [Media Foundation], SetVideoPosition method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetVideoPosition, mf.imfvideodisplaycontrol_setvideoposition
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
 - IMFVideoDisplayControl::SetVideoPosition
 - evr/IMFVideoDisplayControl::SetVideoPosition
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
 - IMFVideoDisplayControl.SetVideoPosition
archived: true
---

# IMFVideoDisplayControl::SetVideoPosition


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the source and destination rectangles for the video.

## -parameters

### -param pnrcSource [in]

Pointer to an <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure that specifies the source rectangle. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the source rectangle does not change.

### -param prcDest [in]

Specifies the destination rectangle. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the destination rectangle does not change.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one parameter must be non-<b>NULL</b>.

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

The source rectangle defines which portion of the video is displayed. It is specified in <i>normalized</i> coordinates. For more information, see <a href="/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect">MFVideoNormalizedRect</a> structure. To display the entire video image, set the source rectangle to {0, 0, 1, 1}. The default source rectangle is {0, 0, 1, 1}.

The destination rectangle defines a rectangle within the clipping window where the video appears. It is specified in pixels, relative to the client area of the window. To fill the entire window, set the destination rectangle to {0, 0, <i>width</i>, <i>height</i>}, where <i>width</i> and <i>height</i> are dimensions of the window client area. The default destination rectangle is {0, 0, 0, 0}.

To update just one of these rectangles, set the other parameter to <b>NULL</b>. You can set <i>pnrcSource</i> or <i>prcDest</i> to <b>NULL</b>, but not both.

Before setting the destination rectangle (<i>prcDest</i>), you must set the video window by calling <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow">IMFVideoDisplayControl::SetVideoWindow</a>. (For the Media Foundation version of the EVR, you can also provide the video window in the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate">MFCreateVideoRendererActivate</a> function.) If no video window was provided, <b>SetVideoPosition</b> returns E_POINTER.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>