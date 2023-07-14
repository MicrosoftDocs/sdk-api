---
UID: NF:segment.IMSVidStreamBufferSink.get_SBESink
title: IMSVidStreamBufferSink::get_SBESink (segment.h)
description: The get_SBESink method retrieves a pointer to the Stream Buffer Sink filter.
helpviewer_keywords: ["IMSVidStreamBufferSink interface [Microsoft TV Technologies]","get_SBESink method","IMSVidStreamBufferSink.get_SBESink","IMSVidStreamBufferSink::get_SBESink","IMSVidStreamBufferSinkget_DVRConfigure","get_SBESink","get_SBESink method [Microsoft TV Technologies]","get_SBESink method [Microsoft TV Technologies]","IMSVidStreamBufferSink interface","mstv.imsvidstreambuffersink_get_sbesink","segment/IMSVidStreamBufferSink::get_SBESink"]
old-location: mstv\imsvidstreambuffersink_get_sbesink.htm
tech.root: mstv
ms.assetid: ea911a70-1926-4ba8-b9dd-1188debee00a
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink interface [Microsoft TV Technologies],get_SBESink method, IMSVidStreamBufferSink.get_SBESink, IMSVidStreamBufferSink::get_SBESink, IMSVidStreamBufferSinkget_DVRConfigure, get_SBESink, get_SBESink method [Microsoft TV Technologies], get_SBESink method [Microsoft TV Technologies],IMSVidStreamBufferSink interface, mstv.imsvidstreambuffersink_get_sbesink, segment/IMSVidStreamBufferSink::get_SBESink
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
 - IMSVidStreamBufferSink::get_SBESink
 - segment/IMSVidStreamBufferSink::get_SBESink
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
 - IMSVidStreamBufferSink.get_SBESink
---

# IMSVidStreamBufferSink::get_SBESink


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SBESink</b> method retrieves a pointer to the <a href="/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter.

## -parameters

### -param sbeConfig [out]

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

<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersink">IMSVidStreamBufferSink Interface</a>