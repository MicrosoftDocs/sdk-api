---
UID: NF:segment.IMSVidClosedCaptioning.put_Enable
title: IMSVidClosedCaptioning::put_Enable (segment.h)
description: The put_Enable method enables or disables closed captioning.
helpviewer_keywords: ["IMSVidClosedCaptioning interface [Microsoft TV Technologies]","put_Enable method","IMSVidClosedCaptioning.put_Enable","IMSVidClosedCaptioning::put_Enable","IMSVidClosedCaptioningput_Enable","mstv.imsvidclosedcaptioning_put_enable","put_Enable","put_Enable method [Microsoft TV Technologies]","put_Enable method [Microsoft TV Technologies]","IMSVidClosedCaptioning interface","segment/IMSVidClosedCaptioning::put_Enable"]
old-location: mstv\imsvidclosedcaptioning_put_enable.htm
tech.root: mstv
ms.assetid: 2485b634-24e9-4945-ae46-0ca7fdb9d92b
ms.date: 12/05/2018
ms.keywords: IMSVidClosedCaptioning interface [Microsoft TV Technologies],put_Enable method, IMSVidClosedCaptioning.put_Enable, IMSVidClosedCaptioning::put_Enable, IMSVidClosedCaptioningput_Enable, mstv.imsvidclosedcaptioning_put_enable, put_Enable, put_Enable method [Microsoft TV Technologies], put_Enable method [Microsoft TV Technologies],IMSVidClosedCaptioning interface, segment/IMSVidClosedCaptioning::put_Enable
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
 - IMSVidClosedCaptioning::put_Enable
 - segment/IMSVidClosedCaptioning::put_Enable
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
 - IMSVidClosedCaptioning.put_Enable
---

# IMSVidClosedCaptioning::put_Enable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Enable</b> method enables or disables closed captioning.

## -parameters

### -param On [in]

Specifies whether to enable or disable the closed captioning feature. Use one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Enable closed captioning.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Disable closed captioning.</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidclosedcaptioning">IMSVidClosedCaptioning Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidclosedcaptioning-get_enable">IMSVidClosedCaptioning::get_Enable</a>