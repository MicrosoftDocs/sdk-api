---
UID: NF:segment.IMSVidPlayback.get_Length
title: IMSVidPlayback::get_Length (segment.h)
description: The get_Length method retrieves the length of the playback source.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","get_Length method","IMSVidPlayback.get_Length","IMSVidPlayback::get_Length","IMSVidPlaybackget_Length","get_Length","get_Length method [Microsoft TV Technologies]","get_Length method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_get_length","segment/IMSVidPlayback::get_Length"]
old-location: mstv\imsvidplayback_get_length.htm
tech.root: mstv
ms.assetid: a559c0b4-ed63-47ef-b99a-866c87939d5b
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_Length method, IMSVidPlayback.get_Length, IMSVidPlayback::get_Length, IMSVidPlaybackget_Length, get_Length, get_Length method [Microsoft TV Technologies], get_Length method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_length, segment/IMSVidPlayback::get_Length
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
 - IMSVidPlayback::get_Length
 - segment/IMSVidPlayback::get_Length
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
 - IMSVidPlayback.get_Length
---

# IMSVidPlayback::get_Length


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Length</b> method retrieves the length of the playback source.

## -parameters

### -param lLength [out]

Pointer to a variable that receives the length. The units for the returned value are determined by the current position mode.

<table>
<tr>
<th>Position Mode
                </th>
<th>Returned Value
                </th>
</tr>
<tr>
<td>FrameMode</td>
<td>Frame number</td>
</tr>
<tr>
<td>TenthsSecondsMode</td>
<td>Hundredths of seconds</td>
</tr>
</table>
 

To set the position mode, call <a href="/windows/desktop/api/segment/nf-segment-imsvidplayback-put_positionmode">IMSVidPlayback::put_PositionMode</a>.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The source does not support getting the length.

</td>
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

## -remarks

Call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-build">IMSVidCtl::Build</a> or <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method before calling this method.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>