---
UID: NF:segment.IMSVidClosedCaptioning2.put_Service
title: IMSVidClosedCaptioning2::put_Service (segment.h)
description: The get_Service method sets the closed captioning service.
helpviewer_keywords: ["IMSVidClosedCaptioning2 interface [Microsoft TV Technologies]","put_Service method","IMSVidClosedCaptioning2.put_Service","IMSVidClosedCaptioning2::put_Service","IMSVidClosedCaptioning2put_Service","mstv.imsvidclosedcaptioning2_put_service","put_Service","put_Service method [Microsoft TV Technologies]","put_Service method [Microsoft TV Technologies]","IMSVidClosedCaptioning2 interface","segment/IMSVidClosedCaptioning2::put_Service"]
old-location: mstv\imsvidclosedcaptioning2_put_service.htm
tech.root: mstv
ms.assetid: f638a7c3-bd0a-465d-b104-ea0066aec6d6
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning2 interface [Microsoft TV Technologies],put_Service method, IMSVidClosedCaptioning2.put_Service, IMSVidClosedCaptioning2::put_Service, IMSVidClosedCaptioning2put_Service, mstv.imsvidclosedcaptioning2_put_service, put_Service, put_Service method [Microsoft TV Technologies], put_Service method [Microsoft TV Technologies],IMSVidClosedCaptioning2 interface, segment/IMSVidClosedCaptioning2::put_Service
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
 - IMSVidClosedCaptioning2::put_Service
 - segment/IMSVidClosedCaptioning2::put_Service
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
 - IMSVidClosedCaptioning2.put_Service
---

# IMSVidClosedCaptioning2::put_Service


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Service</b> method sets the closed captioning service.

## -parameters

### -param On [in]

Specifies the closed captioning service, as a member of the <a href="/windows/desktop/api/segment/ne-segment-msvidccservice">MSVidCCService</a> enumeration.

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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidclosedcaptioning2">IMSVidClosedCaptioning2 Interface</a>