---
UID: NF:segment.IMSVidPlayback.Run
title: IMSVidPlayback::Run (segment.h)
description: The Run method runs the playback device.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","Run method","IMSVidPlayback.Run","IMSVidPlayback::Run","IMSVidPlaybackRun","Run","Run method [Microsoft TV Technologies]","Run method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_run","segment/IMSVidPlayback::Run"]
old-location: mstv\imsvidplayback_run.htm
tech.root: mstv
ms.assetid: 58374819-82dd-4ffe-8cd7-ad51ea0d7207
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Run method, IMSVidPlayback.Run, IMSVidPlayback::Run, IMSVidPlaybackRun, Run, Run method [Microsoft TV Technologies], Run method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_run, segment/IMSVidPlayback::Run
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
 - IMSVidPlayback::Run
 - segment/IMSVidPlayback::Run
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
 - IMSVidPlayback.Run
---

# IMSVidPlayback::Run


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Run</b> method runs the playback device.

Applications should call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-run">IMSVidCtl::Run</a> method, rather than this method.



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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method allows for direct control of the source. However, if the underlying source filter is controlled using the standard DirectShow <a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl</a> interface, this method returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>
