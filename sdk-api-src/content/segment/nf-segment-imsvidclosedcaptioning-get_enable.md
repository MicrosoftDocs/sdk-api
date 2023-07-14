---
UID: NF:segment.IMSVidClosedCaptioning.get_Enable
title: IMSVidClosedCaptioning::get_Enable (segment.h)
description: The get_Enable method queries whether closed captioning is enabled.
helpviewer_keywords: ["IMSVidClosedCaptioning interface [Microsoft TV Technologies]","get_Enable method","IMSVidClosedCaptioning.get_Enable","IMSVidClosedCaptioning::get_Enable","IMSVidClosedCaptioningget_Enable","get_Enable","get_Enable method [Microsoft TV Technologies]","get_Enable method [Microsoft TV Technologies]","IMSVidClosedCaptioning interface","mstv.imsvidclosedcaptioning_get_enable","segment/IMSVidClosedCaptioning::get_Enable"]
old-location: mstv\imsvidclosedcaptioning_get_enable.htm
tech.root: mstv
ms.assetid: 2bb46aa7-fd94-4afa-9bba-769472e014ff
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning interface [Microsoft TV Technologies],get_Enable method, IMSVidClosedCaptioning.get_Enable, IMSVidClosedCaptioning::get_Enable, IMSVidClosedCaptioningget_Enable, get_Enable, get_Enable method [Microsoft TV Technologies], get_Enable method [Microsoft TV Technologies],IMSVidClosedCaptioning interface, mstv.imsvidclosedcaptioning_get_enable, segment/IMSVidClosedCaptioning::get_Enable
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
 - IMSVidClosedCaptioning::get_Enable
 - segment/IMSVidClosedCaptioning::get_Enable
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
 - IMSVidClosedCaptioning.get_Enable
---

# IMSVidClosedCaptioning::get_Enable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Enable</b> method queries whether closed captioning is enabled.

## -parameters

### -param On [out]

Pointer to a variable that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Closed captioning is enabled.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Closed captioning is disabled.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidclosedcaptioning">IMSVidClosedCaptioning Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidclosedcaptioning-put_enable">IMSVidClosedCaptioning::put_Enable</a>