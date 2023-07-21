---
UID: NF:segment.IMSVidClosedCaptioning2.get_Service
title: IMSVidClosedCaptioning2::get_Service (segment.h)
description: The get_Service method retrieves the current closed captioning service.
helpviewer_keywords: ["IMSVidClosedCaptioning2 interface [Microsoft TV Technologies]","get_Service method","IMSVidClosedCaptioning2.get_Service","IMSVidClosedCaptioning2::get_Service","IMSVidClosedCaptioning2get_Service","get_Service","get_Service method [Microsoft TV Technologies]","get_Service method [Microsoft TV Technologies]","IMSVidClosedCaptioning2 interface","mstv.imsvidclosedcaptioning2_get_service","segment/IMSVidClosedCaptioning2::get_Service"]
old-location: mstv\imsvidclosedcaptioning2_get_service.htm
tech.root: mstv
ms.assetid: 165e5c75-3ce1-4b37-b577-5aea4af65019
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning2 interface [Microsoft TV Technologies],get_Service method, IMSVidClosedCaptioning2.get_Service, IMSVidClosedCaptioning2::get_Service, IMSVidClosedCaptioning2get_Service, get_Service, get_Service method [Microsoft TV Technologies], get_Service method [Microsoft TV Technologies],IMSVidClosedCaptioning2 interface, mstv.imsvidclosedcaptioning2_get_service, segment/IMSVidClosedCaptioning2::get_Service
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
 - IMSVidClosedCaptioning2::get_Service
 - segment/IMSVidClosedCaptioning2::get_Service
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
 - IMSVidClosedCaptioning2.get_Service
---

# IMSVidClosedCaptioning2::get_Service


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Service</b> method retrieves the current closed captioning service.

## -parameters

### -param On [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/segment/ne-segment-msvidccservice">MSVidCCService</a> enumeration.

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

<a href="/windows/desktop/api/segment/nn-segment-imsvidclosedcaptioning2">IMSVidClosedCaptioning2 Interface</a>