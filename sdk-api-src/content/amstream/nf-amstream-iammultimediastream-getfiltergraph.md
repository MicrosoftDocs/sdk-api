---
UID: NF:amstream.IAMMultiMediaStream.GetFilterGraph
title: IAMMultiMediaStream::GetFilterGraph (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetFilterGraph method retrieves the Filter Graph Manager that is managed by the multimedia stream object.
helpviewer_keywords: ["GetFilterGraph","GetFilterGraph method [DirectShow]","GetFilterGraph method [DirectShow]","IAMMultiMediaStream interface","IAMMultiMediaStream interface [DirectShow]","GetFilterGraph method","IAMMultiMediaStream.GetFilterGraph","IAMMultiMediaStream::GetFilterGraph","IAMMultiMediaStreamGetFilterGraph","amstream/IAMMultiMediaStream::GetFilterGraph","dshow.iammultimediastream_getfiltergraph"]
old-location: dshow\iammultimediastream_getfiltergraph.htm
tech.root: dshow
ms.assetid: 7e772ced-d14e-45da-9e97-36579e7e3ffd
ms.date: 12/05/2018
ms.keywords: GetFilterGraph, GetFilterGraph method [DirectShow], GetFilterGraph method [DirectShow],IAMMultiMediaStream interface, IAMMultiMediaStream interface [DirectShow],GetFilterGraph method, IAMMultiMediaStream.GetFilterGraph, IAMMultiMediaStream::GetFilterGraph, IAMMultiMediaStreamGetFilterGraph, amstream/IAMMultiMediaStream::GetFilterGraph, dshow.iammultimediastream_getfiltergraph
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IAMMultiMediaStream::GetFilterGraph
 - amstream/IAMMultiMediaStream::GetFilterGraph
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMultiMediaStream.GetFilterGraph
---

# IAMMultiMediaStream::GetFilterGraph


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFilterGraph</code> method retrieves the Filter Graph Manager that is managed by the multimedia stream object.

## -parameters

### -param ppGraphBuilder [out]

Address of a variable that receives an <a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface pointer. If there is no filter graph associated with the multimedia stream object, the returned pointer is <b>NULL</b>.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

If the method succeeds and *<i>ppGraphBuilder</i> is non-<b>NULL</b>, the caller must release the <b>IGraphBuilder</b> pointer.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>