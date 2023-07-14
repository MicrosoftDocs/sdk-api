---
UID: NF:segment.IMSVidPlayback.get_Rate
title: IMSVidPlayback::get_Rate (segment.h)
description: The get_Rate method retrieves the playback rate.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","get_Rate method","IMSVidPlayback.get_Rate","IMSVidPlayback::get_Rate","IMSVidPlaybackget_Rate","get_Rate","get_Rate method [Microsoft TV Technologies]","get_Rate method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_get_rate","segment/IMSVidPlayback::get_Rate"]
old-location: mstv\imsvidplayback_get_rate.htm
tech.root: mstv
ms.assetid: 2f91c728-23c7-4559-9c72-ddd92b0b0212
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_Rate method, IMSVidPlayback.get_Rate, IMSVidPlayback::get_Rate, IMSVidPlaybackget_Rate, get_Rate, get_Rate method [Microsoft TV Technologies], get_Rate method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_rate, segment/IMSVidPlayback::get_Rate
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
 - IMSVidPlayback::get_Rate
 - segment/IMSVidPlayback::get_Rate
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
 - IMSVidPlayback.get_Rate
---

# IMSVidPlayback::get_Rate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Rate</b> method retrieves the playback rate.

## -parameters

### -param plRate [out]

Pointer to a variable that receives the playback rate, as a ratio to the authored rate. For example, 0.5 means half the normal speed, 1.0 means normal speed, and 2.0 means twice the normal speed.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>