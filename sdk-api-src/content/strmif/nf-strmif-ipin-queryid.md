---
UID: NF:strmif.IPin.QueryId
title: IPin::QueryId (strmif.h)
description: The QueryId method retrieves an identifier for the pin.
helpviewer_keywords: ["IPin interface [DirectShow]","QueryId method","IPin.QueryId","IPin::QueryId","IPinQueryId","QueryId","QueryId method [DirectShow]","QueryId method [DirectShow]","IPin interface","dshow.ipin_queryid","strmif/IPin::QueryId"]
old-location: dshow\ipin_queryid.htm
tech.root: dshow
ms.assetid: d4fb2713-549d-4c0d-9768-386bcffd696f
ms.date: 12/05/2018
ms.keywords: IPin interface [DirectShow],QueryId method, IPin.QueryId, IPin::QueryId, IPinQueryId, QueryId, QueryId method [DirectShow], QueryId method [DirectShow],IPin interface, dshow.ipin_queryid, strmif/IPin::QueryId
f1_keywords:
- strmif/IPin.QueryId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IPin.QueryId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPin::QueryId


## -description



The <code>QueryId</code> method retrieves an identifier for the pin.




## -parameters




### -param Id [out]

Receives a string containing the pin identifier.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method supports graph persistence. Use this method to save a pin's state, and the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ibasefilter-findpin">IBaseFilter::FindPin</a> method to restore the state. The pin's identifier string is defined by the filter implementation. The identifier must be unique within the filter.

<div class="alert"><b>Note</b>  The <i>pin identifier</i> is not necessarily the same as the <i>pin name</i> that the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-querypininfo">QueryPinInfo</a> method returns.</div>
<div> </div>
The filter allocates the returned string using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function. The caller must free it using <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
 

 

