---
UID: NF:strmif.ICaptureGraphBuilder2.SetFiltergraph
title: ICaptureGraphBuilder2::SetFiltergraph (strmif.h)
description: The SetFiltergraph method specifies a filter graph for the capture graph builder to use.
helpviewer_keywords: ["ICaptureGraphBuilder2 interface [DirectShow]","SetFiltergraph method","ICaptureGraphBuilder2.SetFiltergraph","ICaptureGraphBuilder2::SetFiltergraph","ICaptureGraphBuilder2SetFiltergraph","SetFiltergraph","SetFiltergraph method [DirectShow]","SetFiltergraph method [DirectShow]","ICaptureGraphBuilder2 interface","dshow.icapturegraphbuilder2_setfiltergraph","strmif/ICaptureGraphBuilder2::SetFiltergraph"]
old-location: dshow\icapturegraphbuilder2_setfiltergraph.htm
tech.root: dshow
ms.assetid: 6193ece8-cdf1-44f5-9619-16380352193f
ms.date: 12/05/2018
ms.keywords: ICaptureGraphBuilder2 interface [DirectShow],SetFiltergraph method, ICaptureGraphBuilder2.SetFiltergraph, ICaptureGraphBuilder2::SetFiltergraph, ICaptureGraphBuilder2SetFiltergraph, SetFiltergraph, SetFiltergraph method [DirectShow], SetFiltergraph method [DirectShow],ICaptureGraphBuilder2 interface, dshow.icapturegraphbuilder2_setfiltergraph, strmif/ICaptureGraphBuilder2::SetFiltergraph
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
 - ICaptureGraphBuilder2::SetFiltergraph
 - strmif/ICaptureGraphBuilder2::SetFiltergraph
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
 - ICaptureGraphBuilder2.SetFiltergraph
---

# ICaptureGraphBuilder2::SetFiltergraph


## -description

The <code>SetFiltergraph</code> method specifies a filter graph for the capture graph builder to use.

## -parameters

### -param pfg [in]

Pointer to the filter graph's <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>

## -remarks

If you do not call this method, the capture graph builder automatically creates a filter graph when it needs one. If the capture graph builder already has a filter graph, this method returns E_UNEXPECTED.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>