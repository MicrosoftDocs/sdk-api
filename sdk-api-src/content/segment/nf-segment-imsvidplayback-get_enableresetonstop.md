---
UID: NF:segment.IMSVidPlayback.get_EnableResetOnStop
title: IMSVidPlayback::get_EnableResetOnStop (segment.h)
description: The get_EnableResetOnStop method indicates how playback will resume if the graph is rebuilt.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","get_EnableResetOnStop method","IMSVidPlayback.get_EnableResetOnStop","IMSVidPlayback::get_EnableResetOnStop","IMSVidPlaybackget_EnableResetOnStop","get_EnableResetOnStop","get_EnableResetOnStop method [Microsoft TV Technologies]","get_EnableResetOnStop method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_get_enableresetonstop","segment/IMSVidPlayback::get_EnableResetOnStop"]
old-location: mstv\imsvidplayback_get_enableresetonstop.htm
tech.root: mstv
ms.assetid: 0ea9ad29-9903-41ac-9be8-acb41cec10d1
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_EnableResetOnStop method, IMSVidPlayback.get_EnableResetOnStop, IMSVidPlayback::get_EnableResetOnStop, IMSVidPlaybackget_EnableResetOnStop, get_EnableResetOnStop, get_EnableResetOnStop method [Microsoft TV Technologies], get_EnableResetOnStop method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_enableresetonstop, segment/IMSVidPlayback::get_EnableResetOnStop
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
 - IMSVidPlayback::get_EnableResetOnStop
 - segment/IMSVidPlayback::get_EnableResetOnStop
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
 - IMSVidPlayback.get_EnableResetOnStop
---

# IMSVidPlayback::get_EnableResetOnStop


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_EnableResetOnStop</b> method indicates how playback will resume if the graph is rebuilt.

## -parameters

### -param pVal [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control will not seek to start of the media.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control will seek to start of the media.</td>
</tr>
</table>

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidplayback-put_enableresetonstop">IMSVidPlayback::put_EnableResetOnStop</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>