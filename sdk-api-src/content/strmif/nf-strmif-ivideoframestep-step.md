---
UID: NF:strmif.IVideoFrameStep.Step
title: IVideoFrameStep::Step (strmif.h)
description: The Step method causes the filter graph to step forward by the specified number of frames.
helpviewer_keywords: ["IVideoFrameStep interface [DirectShow]","Step method","IVideoFrameStep.Step","IVideoFrameStep::Step","IVideoFrameStepStep","Step","Step method [DirectShow]","Step method [DirectShow]","IVideoFrameStep interface","dshow.ivideoframestep_step","strmif/IVideoFrameStep::Step"]
old-location: dshow\ivideoframestep_step.htm
tech.root: dshow
ms.assetid: 1366b8b4-ea7a-4528-8a5a-03a3de265d89
ms.date: 4/26/2023
ms.keywords: IVideoFrameStep interface [DirectShow],Step method, IVideoFrameStep.Step, IVideoFrameStep::Step, IVideoFrameStepStep, Step, Step method [DirectShow], Step method [DirectShow],IVideoFrameStep interface, dshow.ivideoframestep_step, strmif/IVideoFrameStep::Step
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVideoFrameStep::Step
 - strmif/IVideoFrameStep::Step
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
 - IVideoFrameStep.Step
---

# IVideoFrameStep::Step


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Step</code> method causes the filter graph to step forward by the specified number of frames.

## -parameters

### -param dwFrames

Specifies the number of frames to skip. If <i>dwFrames</i> is 1, the graph steps forward one frame. If <i>dwFrames</i> is a number <i>n</i> greater than 1, the graph skips <i>n</i> - 1 frames and shows the <i>n</i>th frame.

### -param pStepObject

Pointer to an interface on the filter that will control the stepping operation, or <b>NULL</b>. Specify <b>NULL</b> to perform the frame stepping using the renderer filter in the graph. If non-<b>NULL</b>, the object must implement the <a href="/windows/desktop/DirectShow/ikspropertyset">IKsPropertySet</a> interface and support the AM_KSPROPSETID_FrameStep property. (For more information, see <a href="/windows/desktop/DirectShow/frame-stepping-property-set">Frame Stepping Property Set</a>.) If the graph includes a custom filter that implements the frame stepping, <i>pStepObject</i> can specify a pointer to that filter.

## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_FRAME_STEP_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Frame stepping is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pStepObject</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

When the step operation is complete, this method sends an <a href="/windows/desktop/DirectShow/ec-step-complete">EC_STEP_COMPLETE</a> event notification to the filter graph manager, which will pass it to the application's event loop and set the filter graph to a paused state.

The frames step in real time, which means that if the movie is playing at 30 frames per second, calling <b>IVideoFrameStep::Step</b> with <i>dwFrames</i> set to 60 would take 2 seconds to execute. All methods in this interface are asynchronous, so control returns to the application immediately.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivideoframestep">IVideoFrameStep Interface</a>