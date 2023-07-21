---
UID: NF:segment.IMSVidPlayback.Stop
title: IMSVidPlayback::Stop (segment.h)
description: The Stop method stops the playback device.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","Stop method","IMSVidPlayback.Stop","IMSVidPlayback::Stop","IMSVidPlaybackStop","Stop","Stop method [Microsoft TV Technologies]","Stop method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_stop","segment/IMSVidPlayback::Stop"]
old-location: mstv\imsvidplayback_stop.htm
tech.root: mstv
ms.assetid: 20262521-bb9c-4e37-b89c-8c439df50ed4
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Stop method, IMSVidPlayback.Stop, IMSVidPlayback::Stop, IMSVidPlaybackStop, Stop, Stop method [Microsoft TV Technologies], Stop method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_stop, segment/IMSVidPlayback::Stop
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
 - IMSVidPlayback::Stop
 - segment/IMSVidPlayback::Stop
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
 - IMSVidPlayback.Stop
---

# IMSVidPlayback::Stop


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Stop</b> method stops the playback device.

Applications should call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-stop">IMSVidCtl::Stop</a> method, rather than this method.



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
