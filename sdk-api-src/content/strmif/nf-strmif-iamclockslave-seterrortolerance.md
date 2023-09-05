---
UID: NF:strmif.IAMClockSlave.SetErrorTolerance
title: IAMClockSlave::SetErrorTolerance (strmif.h)
description: The SetErrorTolerance method sets the audio renderer's rate-matching tolerance.
helpviewer_keywords: ["IAMClockSlave interface [DirectShow]","SetErrorTolerance method","IAMClockSlave.SetErrorTolerance","IAMClockSlave::SetErrorTolerance","IAMClockSlaveSetErrorTolerance","SetErrorTolerance","SetErrorTolerance method [DirectShow]","SetErrorTolerance method [DirectShow]","IAMClockSlave interface","dshow.iamclockslave_seterrortolerance","strmif/IAMClockSlave::SetErrorTolerance"]
old-location: dshow\iamclockslave_seterrortolerance.htm
tech.root: dshow
ms.assetid: 6c93e345-4e4a-4019-9c18-d3d43736fee3
ms.date: 4/26/2023
ms.keywords: IAMClockSlave interface [DirectShow],SetErrorTolerance method, IAMClockSlave.SetErrorTolerance, IAMClockSlave::SetErrorTolerance, IAMClockSlaveSetErrorTolerance, SetErrorTolerance, SetErrorTolerance method [DirectShow], SetErrorTolerance method [DirectShow],IAMClockSlave interface, dshow.iamclockslave_seterrortolerance, strmif/IAMClockSlave::SetErrorTolerance
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IAMClockSlave::SetErrorTolerance
 - strmif/IAMClockSlave::SetErrorTolerance
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
 - IAMClockSlave.SetErrorTolerance
---

# IAMClockSlave::SetErrorTolerance


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetErrorTolerance</code> method sets the audio renderer's rate-matching tolerance.

## -parameters

### -param dwTolerance [in]

Specifies the maximum tolerance, in milliseconds. The value must be from 1 to 1000, inclusive.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>

## -remarks

Changing the tolerance has no effect unless the audio renderer is matching rates with a different clock. If the audio renderer is the reference clock, the audio is always synchronized to the clock (by definition).

This method fails if the filter graph is not stopped.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamclockslave">IAMClockSlave Interface</a>