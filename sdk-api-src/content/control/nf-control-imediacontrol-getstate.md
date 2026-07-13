---
UID: NF:control.IMediaControl.GetState
title: IMediaControl::GetState (control.h)
description: The GetState method retrieves the state of the filter graph - paused, running, or stopped.
helpviewer_keywords: ["GetState","GetState method [DirectShow]","GetState method [DirectShow]","IMediaControl interface","IMediaControl interface [DirectShow]","GetState method","IMediaControl.GetState","IMediaControl::GetState","IMediaControlGetState","control/IMediaControl::GetState","dshow.imediacontrol_getstate"]
old-location: dshow\imediacontrol_getstate.htm
tech.root: dshow
ms.assetid: 653a94ff-6929-41b1-9b94-dccaff0f7ec7
ms.date: 4/26/2023
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IMediaControl interface, IMediaControl interface [DirectShow],GetState method, IMediaControl.GetState, IMediaControl::GetState, IMediaControlGetState, control/IMediaControl::GetState, dshow.imediacontrol_getstate
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
 - IMediaControl::GetState
 - control/IMediaControl::GetState
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
 - IMediaControl.GetState
---

# IMediaControl::GetState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetState</code> method retrieves the state of the filter graph—paused, running, or stopped.



State transitions are not necessarily synchronous. Therefore, when you call this method, the filter graph might be in transition to a new state. In that case, the method blocks until the transition completes or until the specified time-out elapses.

## -parameters

### -param msTimeout [in]

Duration of the time-out, in milliseconds, or INFINITE to specify an infinite time-out.

### -param pfs [out]

Receives a member of the [FILTER_STATE](/windows/desktop/api/strmif/ne-strmif-filter_state) enumeration.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>VFW_S_STATE_INTERMEDIATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is still in transition to the indicated state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_CANT_CUE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is paused, but cannot cue data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
</table>

## -remarks

Applications can use this method to determine whether playback has started after a call to <a href="/windows/desktop/api/control/nf-control-imediacontrol-run">IMediaControl::Run</a>. Generally, applications should have their own mechanism for tracking which state they have put the filter graph into. Applications typically use the current state to determine which user interface controls are enabled or disabled. For example, once the graph goes into the running state, the application might disable a "Play" button and enable "Stop" and "Pause" buttons.

If the filter graph is in a transition to a new state, the returned state is the new state, not the previous state.

This method returns an error if there is a call on another thread to change the state while this method is blocked.

Avoid specifying a time-out of INFINITE, because threads cannot process messages while waiting in <code>GetState</code>. If you call <code>GetState</code> from the thread that processes Windows messages, specify small wait times on the call in order to remain responsive to user input. This is especially important when the source is streaming over a network or from the Internet because state transitions in these environments can take significantly more time to complete.

The [FILTER_STATE](/windows/desktop/api/strmif/ne-strmif-filter_state) enumeration. You can cast the variable as follows:


```cpp

FILTER_STATE fs;
hr = pControl->GetState(msTimeOut, (OAFilterState*)&fs);

```


For more information about filter graph states, see <a href="/windows/desktop/DirectShow/filter-states">Filter States</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>
