---
UID: NF:strmif.IMediaFilter.Stop
title: IMediaFilter::Stop (strmif.h)
description: The Stop method stops the filter.
helpviewer_keywords: ["IMediaFilter interface [DirectShow]","Stop method","IMediaFilter.Stop","IMediaFilter::Stop","IMediaFilterStop","Stop","Stop method [DirectShow]","Stop method [DirectShow]","IMediaFilter interface","dshow.imediafilter_stop","strmif/IMediaFilter::Stop"]
old-location: dshow\imediafilter_stop.htm
tech.root: dshow
ms.assetid: 8c415b5c-1aee-4ea4-b182-fd95da4898aa
ms.date: 12/05/2018
ms.keywords: IMediaFilter interface [DirectShow],Stop method, IMediaFilter.Stop, IMediaFilter::Stop, IMediaFilterStop, Stop, Stop method [DirectShow], Stop method [DirectShow],IMediaFilter interface, dshow.imediafilter_stop, strmif/IMediaFilter::Stop
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMediaFilter::Stop
 - strmif/IMediaFilter::Stop
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
 - IMediaFilter.Stop
---

# IMediaFilter::Stop


## -description

The <code>Stop</code> method stops the filter.

## -parameters

## -returns

Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Transition is not complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success. Transition is complete.

</td>
</tr>
</table>

## -remarks

When a filter is stopped, it does not process or deliver any samples, and it rejects samples from upstream filters.

The state transition might be asynchronous. If the method returns before the transition completes, the return value is S_FALSE.

This method always sets the filter's state to State_Stopped, even if the method returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



[FILTER_STATE Enumeration](/windows/desktop/api/strmif/ne-strmif-filter_state)



<a href="/windows/desktop/api/strmif/nn-strmif-imediafilter">IMediaFilter Interface</a>