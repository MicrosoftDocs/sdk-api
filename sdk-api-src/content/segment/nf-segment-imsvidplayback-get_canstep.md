---
UID: NF:segment.IMSVidPlayback.get_CanStep
title: IMSVidPlayback::get_CanStep (segment.h)
description: The get_CanStep method queries whether the input source can step frame by frame.
helpviewer_keywords: ["IMSVidPlayback interface [Microsoft TV Technologies]","get_CanStep method","IMSVidPlayback.get_CanStep","IMSVidPlayback::get_CanStep","IMSVidPlaybackget_CanStep","get_CanStep","get_CanStep method [Microsoft TV Technologies]","get_CanStep method [Microsoft TV Technologies]","IMSVidPlayback interface","mstv.imsvidplayback_get_canstep","segment/IMSVidPlayback::get_CanStep"]
old-location: mstv\imsvidplayback_get_canstep.htm
tech.root: mstv
ms.assetid: 41aad247-1f04-4245-89df-8ac527926307
ms.date: 12/05/2018
ms.keywords: IMSVidPlayback interface [Microsoft TV Technologies],get_CanStep method, IMSVidPlayback.get_CanStep, IMSVidPlayback::get_CanStep, IMSVidPlaybackget_CanStep, get_CanStep, get_CanStep method [Microsoft TV Technologies], get_CanStep method [Microsoft TV Technologies],IMSVidPlayback interface, mstv.imsvidplayback_get_canstep, segment/IMSVidPlayback::get_CanStep
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
 - IMSVidPlayback::get_CanStep
 - segment/IMSVidPlayback::get_CanStep
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
 - IMSVidPlayback.get_CanStep
---

# IMSVidPlayback::get_CanStep


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CanStep</b> method queries whether the input source can step frame by frame.

## -parameters

### -param fBackwards [in]

Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Query whether the input can step forward</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Query whether the input can step backward.</td>
</tr>
</table>

### -param pfCan [out]

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
<td>The source cannot step in the specified direction.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The source can step in the specified direction.</td>
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


#### Examples


```cpp

VARIANT_BOOL fCan = VARIANT_FALSE;
hr = m_pPlayback->get_CanStep(VARIANT_FALSE, &fCan);

```

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback Interface</a>