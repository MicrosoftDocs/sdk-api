---
UID: NF:strmif.IFilterGraph3.SetSyncSourceEx
title: IFilterGraph3::SetSyncSourceEx (strmif.h)
description: The SetSyncSourceEx method establishes two reference clocks for the filter graph:\_a primary clock that is used by most of the filters, and a secondary clock that is used only by one specified filter.
helpviewer_keywords: ["IFilterGraph3 interface [DirectShow]","SetSyncSourceEx method","IFilterGraph3.SetSyncSourceEx","IFilterGraph3::SetSyncSourceEx","IFilterGraph3SetSyncSourceEx","SetSyncSourceEx","SetSyncSourceEx method [DirectShow]","SetSyncSourceEx method [DirectShow]","IFilterGraph3 interface","dshow.ifiltergraph3_setsyncsourceex","strmif/IFilterGraph3::SetSyncSourceEx"]
old-location: dshow\ifiltergraph3_setsyncsourceex.htm
tech.root: dshow
ms.assetid: 153a0584-d613-499d-8dbb-c4207c7f60b3
ms.date: 12/05/2018
ms.keywords: IFilterGraph3 interface [DirectShow],SetSyncSourceEx method, IFilterGraph3.SetSyncSourceEx, IFilterGraph3::SetSyncSourceEx, IFilterGraph3SetSyncSourceEx, SetSyncSourceEx, SetSyncSourceEx method [DirectShow], SetSyncSourceEx method [DirectShow],IFilterGraph3 interface, dshow.ifiltergraph3_setsyncsourceex, strmif/IFilterGraph3::SetSyncSourceEx
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFilterGraph3::SetSyncSourceEx
 - strmif/IFilterGraph3::SetSyncSourceEx
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
 - IFilterGraph3.SetSyncSourceEx
---

# IFilterGraph3::SetSyncSourceEx


## -description

The <code>SetSyncSourceEx</code> method establishes two reference clocks for the filter graph: a primary clock that is used by most of the filters, and a secondary clock that is used only by one specified filter.

## -parameters

### -param pClockForMostOfFilterGraph [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ireferenceclock">IReferenceClock</a> interface of the main reference clock. Every filter in the graph uses this clock, except for the filter specified by the <i>pFilter</i> parameter.

### -param pClockForFilter [in]

Pointer to the <b>IReferenceClock</b> interface of the secondary clock. The filter specified by the <i>pFilter</i> parameter uses this clock.

### -param pFilter [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of a filter in the graph. This filter uses the secondary reference clock.

## -returns

Returns and <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>

## -remarks

If the filter graph is running or paused, this method return VFW_E_NOT_STOPPED.

To clear both reference clocks, set all three parameters to <b>NULL</b>. To set a single clock for the entire graph, with no secondary clock, call the <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-setsyncsource">IMediaFilter::SetSyncSource</a> method on the Filter Graph Manager.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph3">IFilterGraph3 Interface</a>