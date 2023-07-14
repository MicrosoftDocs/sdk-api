---
UID: NF:segment.IMSVidStreamBufferSource.put_UnratedDelay
title: IMSVidStreamBufferSource::put_UnratedDelay (segment.h)
description: The put_UnratedDelay method specifies how long the Video Control will play unrated content before blocking it. The value is ignored until the put_BlockUnrated method is called with the value VARIANT_TRUE.
helpviewer_keywords: ["IMSVidStreamBufferSource interface [Microsoft TV Technologies]","put_UnratedDelay method","IMSVidStreamBufferSource.put_UnratedDelay","IMSVidStreamBufferSource::put_UnratedDelay","IMSVidStreamBufferSourceput_UnratedDelay","mstv.imsvidstreambuffersource_put_unrateddelay","put_UnratedDelay","put_UnratedDelay method [Microsoft TV Technologies]","put_UnratedDelay method [Microsoft TV Technologies]","IMSVidStreamBufferSource interface","segment/IMSVidStreamBufferSource::put_UnratedDelay"]
old-location: mstv\imsvidstreambuffersource_put_unrateddelay.htm
tech.root: mstv
ms.assetid: 7b4e1ac4-dfb8-45c0-9079-16f8babcb494
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],put_UnratedDelay method, IMSVidStreamBufferSource.put_UnratedDelay, IMSVidStreamBufferSource::put_UnratedDelay, IMSVidStreamBufferSourceput_UnratedDelay, mstv.imsvidstreambuffersource_put_unrateddelay, put_UnratedDelay, put_UnratedDelay method [Microsoft TV Technologies], put_UnratedDelay method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, segment/IMSVidStreamBufferSource::put_UnratedDelay
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
 - IMSVidStreamBufferSource::put_UnratedDelay
 - segment/IMSVidStreamBufferSource::put_UnratedDelay
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
 - IMSVidStreamBufferSource.put_UnratedDelay
---

# IMSVidStreamBufferSource::put_UnratedDelay


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_UnratedDelay</b> method specifies how long the Video Control will play unrated content before blocking it. The value is ignored until the <a href="/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-put_blockunrated">put_BlockUnrated</a> method is called with the value VARIANT_TRUE.

## -parameters

### -param dwDelay [in]

Specifies the delay before blocking unrated content, in milliseconds.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidstreambuffersource-put_blockunrated">IMSVidStreamBufferSource::put_BlockUnrated</a>