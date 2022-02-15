---
UID: NF:strmif.IAMGraphStreams.SetMaxGraphLatency
title: IAMGraphStreams::SetMaxGraphLatency (strmif.h)
description: The SetMaxGraphLatency method sets the maximum latency for the graph. You must call the IAMGraphStreams::SyncUsingStreamOffset method before calling this method.
helpviewer_keywords: ["IAMGraphStreams interface [DirectShow]","SetMaxGraphLatency method","IAMGraphStreams.SetMaxGraphLatency","IAMGraphStreams::SetMaxGraphLatency","IAMGraphStreamsSetMaxGraphLatency","SetMaxGraphLatency","SetMaxGraphLatency method [DirectShow]","SetMaxGraphLatency method [DirectShow]","IAMGraphStreams interface","dshow.iamgraphstreams_setmaxgraphlatency","strmif/IAMGraphStreams::SetMaxGraphLatency"]
old-location: dshow\iamgraphstreams_setmaxgraphlatency.htm
tech.root: dshow
ms.assetid: e17723ad-20b5-4679-94a9-e32efbe82124
ms.date: 12/05/2018
ms.keywords: IAMGraphStreams interface [DirectShow],SetMaxGraphLatency method, IAMGraphStreams.SetMaxGraphLatency, IAMGraphStreams::SetMaxGraphLatency, IAMGraphStreamsSetMaxGraphLatency, SetMaxGraphLatency, SetMaxGraphLatency method [DirectShow], SetMaxGraphLatency method [DirectShow],IAMGraphStreams interface, dshow.iamgraphstreams_setmaxgraphlatency, strmif/IAMGraphStreams::SetMaxGraphLatency
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMGraphStreams::SetMaxGraphLatency
 - strmif/IAMGraphStreams::SetMaxGraphLatency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMGraphStreams.SetMaxGraphLatency
---

# IAMGraphStreams::SetMaxGraphLatency


## -description

The <code>SetMaxGraphLatency</code> method sets the maximum latency for the graph. You must call the <a href="/windows/desktop/api/strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset">IAMGraphStreams::SyncUsingStreamOffset</a> method before calling this method.

## -parameters

### -param rtMaxGraphLatency [in]

Specifies the maximum latency in 100-nanosecond units.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

At connection time, some live source filters use the maximum latency to determine the size of buffer to allocate. Calling this method before constructing the graph can help to ensure that sufficient buffers are allocated for the expected latency.

If you call this method before calling <b>SyncUsingStreamOffset</b>, the method returns E_FAIL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamgraphstreams">IAMGraphStreams Interface</a>