---
UID: NF:segment.IMSVidPlayback.put_Rate
title: IMSVidPlayback::put_Rate (segment.h)
description: The put_Rate method sets the playback rate.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","put_Rate method","IMSVidPlayback.put_Rate","IMSVidPlayback::put_Rate","IMSVidPlaybackput_Rate","mstv.imsvidplayback_put_rate","put_Rate","put_Rate method [Microsoft TV Technologies]","put_Rate method [Microsoft TV Technologies]","IMSVidPlayback interface","segment/IMSVidPlayback::put_Rate"]
old-location: mstv\imsvidplayback_put_rate.htm
tech.root: mstv
ms.assetid: a3542d7c-6333-4832-a24a-0b778ea83a4c
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],put_Rate method, IMSVidPlayback.put_Rate, IMSVidPlayback::put_Rate, IMSVidPlaybackput_Rate, mstv.imsvidplayback_put_rate, put_Rate, put_Rate method [Microsoft TV Technologies], put_Rate method [Microsoft TV Technologies],IMSVidPlayback interface, segment/IMSVidPlayback::put_Rate
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
 - IMSVidPlayback::put_Rate
 - segment/IMSVidPlayback::put_Rate
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
 - IMSVidPlayback.put_Rate
---

# IMSVidPlayback::put_Rate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Rate</b> method sets the playback rate.

## -parameters

### -param plRate [in]

Specifies the playback rate, as a ratio to the authored rate. For example, 0.5 means half the normal speed, 1.0 means normal speed, and 2.0 means twice the normal speed.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The source filter does not support the specified rate.

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

Call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">IMSVidCtl::Build</a> or <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>