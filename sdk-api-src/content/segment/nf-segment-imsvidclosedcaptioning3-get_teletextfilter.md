---
UID: NF:segment.IMSVidClosedCaptioning3.get_TeleTextFilter
title: IMSVidClosedCaptioning3::get_TeleTextFilter (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidClosedCaptioning3 interface [Microsoft TV Technologies]","get_TeleTextFilter method","IMSVidClosedCaptioning3.get_TeleTextFilter","IMSVidClosedCaptioning3::get_TeleTextFilter","IMSVidClosedCaptioning3getTeleTextFilter","get_TeleTextFilter","get_TeleTextFilter method [Microsoft TV Technologies]","get_TeleTextFilter method [Microsoft TV Technologies]","IMSVidClosedCaptioning3 interface","mstv.imsvidclosedcaptioning3_get_teletextfilter","segment/IMSVidClosedCaptioning3::get_TeleTextFilter"]
old-location: mstv\imsvidclosedcaptioning3_get_teletextfilter.htm
tech.root: mstv
ms.assetid: 95376533-e684-4a8e-ac60-6c52bf0f82ae
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning3 interface [Microsoft TV Technologies],get_TeleTextFilter method, IMSVidClosedCaptioning3.get_TeleTextFilter, IMSVidClosedCaptioning3::get_TeleTextFilter, IMSVidClosedCaptioning3getTeleTextFilter, get_TeleTextFilter, get_TeleTextFilter method [Microsoft TV Technologies], get_TeleTextFilter method [Microsoft TV Technologies],IMSVidClosedCaptioning3 interface, mstv.imsvidclosedcaptioning3_get_teletextfilter, segment/IMSVidClosedCaptioning3::get_TeleTextFilter
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidClosedCaptioning3::get_TeleTextFilter
 - segment/IMSVidClosedCaptioning3::get_TeleTextFilter
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
 - IMSVidClosedCaptioning3.get_TeleTextFilter
---

# IMSVidClosedCaptioning3::get_TeleTextFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_TeleTextFilter</b> method retrieves the filter that handles teletext.

## -parameters

### -param punkTTFilter [out]

Pointer to a variable that receives a reference to the teletext filter.

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
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidclosedcaptioning3">IMSVidClosedCaptioning3 Interface</a>