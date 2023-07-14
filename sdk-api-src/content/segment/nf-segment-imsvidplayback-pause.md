---
UID: NF:segment.IMSVidPlayback.Pause
title: IMSVidPlayback::Pause (segment.h)
description: The Pause method pauses the playback device.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","Pause method","IMSVidPlayback.Pause","IMSVidPlayback::Pause","IMSVidPlaybackPause","Pause","Pause method [Microsoft TV Technologies]","Pause method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_pause","segment/IMSVidPlayback::Pause"]
old-location: mstv\imsvidplayback_pause.htm
tech.root: mstv
ms.assetid: 430528b7-3b3a-4df9-8093-9b0f9262f106
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],Pause method, IMSVidPlayback.Pause, IMSVidPlayback::Pause, IMSVidPlaybackPause, Pause, Pause method [Microsoft TV Technologies], Pause method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_pause, segment/IMSVidPlayback::Pause
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
 - IMSVidPlayback::Pause
 - segment/IMSVidPlayback::Pause
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
 - IMSVidPlayback.Pause
---

# IMSVidPlayback::Pause


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Pause</b> method pauses the playback device.

Applications should call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-pause">IMSVidCtl::Pause</a> method, rather than this method.



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
