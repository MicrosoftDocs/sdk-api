---
UID: NF:segment.IMSVidStreamBufferSource.get_SBESource
title: IMSVidStreamBufferSource::get_SBESource (segment.h)
description: The get_SBESource method retrieves a pointer to the Stream Buffer Source filter.
helpviewer_keywords: ["IMSVidStreamBufferSource interface [Microsoft TV Technologies]","get_SBESource method","IMSVidStreamBufferSource.get_SBESource","IMSVidStreamBufferSource::get_SBESource","IMSVidStreamBufferSourceget_SBESource","get_SBESource","get_SBESource method [Microsoft TV Technologies]","get_SBESource method [Microsoft TV Technologies]","IMSVidStreamBufferSource interface","mstv.imsvidstreambuffersource_get_sbesource","segment/IMSVidStreamBufferSource::get_SBESource"]
old-location: mstv\imsvidstreambuffersource_get_sbesource.htm
tech.root: mstv
ms.assetid: 6ba9cf64-bf26-4a17-ae7a-3e92fc67138d
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],get_SBESource method, IMSVidStreamBufferSource.get_SBESource, IMSVidStreamBufferSource::get_SBESource, IMSVidStreamBufferSourceget_SBESource, get_SBESource, get_SBESource method [Microsoft TV Technologies], get_SBESource method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_get_sbesource, segment/IMSVidStreamBufferSource::get_SBESource
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
 - IMSVidStreamBufferSource::get_SBESource
 - segment/IMSVidStreamBufferSource::get_SBESource
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
 - IMSVidStreamBufferSource.get_SBESource
---

# IMSVidStreamBufferSource::get_SBESource


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SBESource</b> method retrieves a pointer to the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-source-filter">Stream Buffer Source</a> filter.

## -parameters

### -param sbeFilter [out]

Receives a pointer to the filter's <b>IUnknown</b> interface.

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

## -remarks

The caller must release the <b>IUnknown</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource Interface</a>