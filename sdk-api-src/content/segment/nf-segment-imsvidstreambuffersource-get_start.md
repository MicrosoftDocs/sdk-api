---
UID: NF:segment.IMSVidStreamBufferSource.get_Start
title: IMSVidStreamBufferSource::get_Start (segment.h)
description: The get_Start method retrieves the start time.
helpviewer_keywords: ["IMSVidStreamBufferSource interface [Microsoft TV Technologies]","get_Start method","IMSVidStreamBufferSource.get_Start","IMSVidStreamBufferSource::get_Start","IMSVidStreamBufferSourceget_Start","get_Start","get_Start method [Microsoft TV Technologies]","get_Start method [Microsoft TV Technologies]","IMSVidStreamBufferSource interface","mstv.imsvidstreambuffersource_get_start","segment/IMSVidStreamBufferSource::get_Start"]
old-location: mstv\imsvidstreambuffersource_get_start.htm
tech.root: mstv
ms.assetid: 4c6ad8b7-93d9-46de-b84a-a4575f3e6183
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],get_Start method, IMSVidStreamBufferSource.get_Start, IMSVidStreamBufferSource::get_Start, IMSVidStreamBufferSourceget_Start, get_Start, get_Start method [Microsoft TV Technologies], get_Start method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_get_start, segment/IMSVidStreamBufferSource::get_Start
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
 - IMSVidStreamBufferSource::get_Start
 - segment/IMSVidStreamBufferSource::get_Start
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
 - IMSVidStreamBufferSource.get_Start
---

# IMSVidStreamBufferSource::get_Start


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Start</b> method retrieves the start time.

## -parameters

### -param lStart [out]

Pointer to a variable that receives the start time, in hundredths of seconds.

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