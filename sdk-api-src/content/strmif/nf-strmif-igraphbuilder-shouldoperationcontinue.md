---
UID: NF:strmif.IGraphBuilder.ShouldOperationContinue
title: IGraphBuilder::ShouldOperationContinue (strmif.h)
description: The ShouldOperationContinue method queries whether the current operation should continue.
helpviewer_keywords: ["IGraphBuilder interface [DirectShow]","ShouldOperationContinue method","IGraphBuilder.ShouldOperationContinue","IGraphBuilder::ShouldOperationContinue","IGraphBuilderShouldOperationContinue","ShouldOperationContinue","ShouldOperationContinue method [DirectShow]","ShouldOperationContinue method [DirectShow]","IGraphBuilder interface","dshow.igraphbuilder_shouldoperationcontinue","strmif/IGraphBuilder::ShouldOperationContinue"]
old-location: dshow\igraphbuilder_shouldoperationcontinue.htm
tech.root: dshow
ms.assetid: 0d862a41-6896-40a5-8bfc-129b15dfc671
ms.date: 12/05/2018
ms.keywords: IGraphBuilder interface [DirectShow],ShouldOperationContinue method, IGraphBuilder.ShouldOperationContinue, IGraphBuilder::ShouldOperationContinue, IGraphBuilderShouldOperationContinue, ShouldOperationContinue, ShouldOperationContinue method [DirectShow], ShouldOperationContinue method [DirectShow],IGraphBuilder interface, dshow.igraphbuilder_shouldoperationcontinue, strmif/IGraphBuilder::ShouldOperationContinue
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
 - IGraphBuilder::ShouldOperationContinue
 - strmif/IGraphBuilder::ShouldOperationContinue
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
 - IGraphBuilder.ShouldOperationContinue
---

# IGraphBuilder::ShouldOperationContinue


## -description

The <code>ShouldOperationContinue</code> method queries whether the current operation should continue. A filter that is performing some operation at the request of the graph can call this method to determine whether it should continue. Applications will not normally call this method.



## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

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
The current operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The current operation should not continue.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>
