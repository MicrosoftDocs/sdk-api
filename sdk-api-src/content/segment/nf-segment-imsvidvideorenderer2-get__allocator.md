---
UID: NF:segment.IMSVidVideoRenderer2.get__Allocator
title: IMSVidVideoRenderer2::get__Allocator (segment.h)
description: The get__Allocator method retrieves the allocator-presenter from the VMR.
helpviewer_keywords: ["IMSVidVideoRenderer2 interface [Microsoft TV Technologies]","get__Allocator method","IMSVidVideoRenderer2.get__Allocator","IMSVidVideoRenderer2::get__Allocator","IMSVidVideoRenderer2get__Allocator","get__Allocator","get__Allocator method [Microsoft TV Technologies]","get__Allocator method [Microsoft TV Technologies]","IMSVidVideoRenderer2 interface","mstv.imsvidvideorenderer2_get__allocator","segment/IMSVidVideoRenderer2::get__Allocator"]
old-location: mstv\imsvidvideorenderer2_get__allocator.htm
tech.root: mstv
ms.assetid: b22d643e-f458-4293-9f2b-e8bfe1499905
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2 interface [Microsoft TV Technologies],get__Allocator method, IMSVidVideoRenderer2.get__Allocator, IMSVidVideoRenderer2::get__Allocator, IMSVidVideoRenderer2get__Allocator, get__Allocator, get__Allocator method [Microsoft TV Technologies], get__Allocator method [Microsoft TV Technologies],IMSVidVideoRenderer2 interface, mstv.imsvidvideorenderer2_get__allocator, segment/IMSVidVideoRenderer2::get__Allocator
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
 - IMSVidVideoRenderer2::get__Allocator
 - segment/IMSVidVideoRenderer2::get__Allocator
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
 - IMSVidVideoRenderer2.get__Allocator
---

# IMSVidVideoRenderer2::get__Allocator


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__Allocator</b> method retrieves the allocator-presenter from the VMR.

## -parameters

### -param AllocPresent [out]

Receives an <a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator</a> interface pointer.

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
</table>

## -remarks

The caller must release the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator</a> interface.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidvideorenderer2">IMSVidVideoRenderer2 Interface</a>