---
UID: NF:segment.IMSVidVideoRenderer2.get_Allocator_ID
title: IMSVidVideoRenderer2::get_Allocator_ID (segment.h)
description: The get_Allocator_ID method retrieves an identifier for the VMR filter's allocator-presenter.
helpviewer_keywords: ["IMSVidVideoRenderer2 interface [Microsoft TV Technologies]","get_Allocator_ID method","IMSVidVideoRenderer2.get_Allocator_ID","IMSVidVideoRenderer2::get_Allocator_ID","IMSVidVideoRenderer2get_Allocator_ID","get_Allocator_ID","get_Allocator_ID method [Microsoft TV Technologies]","get_Allocator_ID method [Microsoft TV Technologies]","IMSVidVideoRenderer2 interface","mstv.imsvidvideorenderer2_get_allocator_id","segment/IMSVidVideoRenderer2::get_Allocator_ID"]
old-location: mstv\imsvidvideorenderer2_get_allocator_id.htm
tech.root: mstv
ms.assetid: 4d512525-ed18-43af-9773-ed56c49c3641
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],get_Allocator_ID method, IMSVidVideoRenderer2.get_Allocator_ID, IMSVidVideoRenderer2::get_Allocator_ID, IMSVidVideoRenderer2get_Allocator_ID, get_Allocator_ID, get_Allocator_ID method [Microsoft TV Technologies], get_Allocator_ID method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2_get_allocator_id, segment/IMSVidVideoRenderer2::get_Allocator_ID
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMSVidVideoRenderer2::get_Allocator_ID
 - segment/IMSVidVideoRenderer2::get_Allocator_ID
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
 - IMSVidVideoRenderer2.get_Allocator_ID
---

# IMSVidVideoRenderer2::get_Allocator_ID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Allocator_ID</b> method retrieves an identifier for the VMR filter's allocator-presenter.

## -parameters

### -param ID [out]

Receives the identifier. If the returned value is -1, the <a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">MSVidVideoRenderer</a> object will assign a default identifier when it builds the filter graph.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The identifier is for application use; it is not used by the VMR.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidvideorenderer2">IMSVidVideoRenderer2 Interface</a>