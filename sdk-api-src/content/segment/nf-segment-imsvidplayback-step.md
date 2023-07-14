---
UID: NF:segment.IMSVidPlayback.Step
title: IMSVidPlayback::Step (segment.h)
description: The Step method steps through the video stream by a specified number of frames.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","Step method","IMSVidPlayback.Step","IMSVidPlayback::Step","IMSVidPlaybackStep","Step","Step method [Microsoft TV Technologies]","Step method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_step","segment/IMSVidPlayback::Step"]
old-location: mstv\imsvidplayback_step.htm
tech.root: mstv
ms.assetid: 8e971571-61f4-4b24-81a7-45fa17b6b785
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Step method, IMSVidPlayback.Step, IMSVidPlayback::Step, IMSVidPlaybackStep, Step, Step method [Microsoft TV Technologies], Step method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_step, segment/IMSVidPlayback::Step
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidPlayback::Step
 - segment/IMSVidPlayback::Step
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidPlayback.Step
---

# IMSVidPlayback::Step


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Step</b> method steps through the video stream by a specified number of frames.

## -parameters

### -param lStep [in]

Specifies how many frames to step. If <i>lStep</i> is 1, the Video Control steps forward one frame. If <i>lStep</i> is a number <i>N</i> greater than 1, the Video Control skips <i>N</i> - 1 frames and shows the <i>N</i>th frame.

## -returns

The method returns an <b>HRESULT</b>. Possible values include the following.

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
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The graph is not built. Call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">Build</a> or <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">View</a> method on the Video Control.

</td>
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
</table>
 

<div class="alert"><b>Note</b>  The value ERROR_INVALID_STATE is converted to an <b>HRESULT</b> with the <b>HRESULT_FROM_WIN32</b> macro.</div>
<div> </div>

## -remarks

Although a negative value for <i>lStep</i> is defined as stepping backward, that functionality is currently not implemented, and the method returns E_NOTIMPL.

Call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">IMSVidCtl::Build</a> or <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidplayback-get_canstep">IMSVidPlayback::get_CanStep</a>