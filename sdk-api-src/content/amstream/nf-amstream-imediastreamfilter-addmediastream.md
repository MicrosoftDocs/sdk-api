---
UID: NF:amstream.IMediaStreamFilter.AddMediaStream
title: IMediaStreamFilter::AddMediaStream (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The AddMediaStream method connects a media stream object to the underlying filter graph.
helpviewer_keywords: ["AddMediaStream","AddMediaStream method [DirectShow]","AddMediaStream method [DirectShow]","IMediaStreamFilter interface","IMediaStreamFilter interface [DirectShow]","AddMediaStream method","IMediaStreamFilter.AddMediaStream","IMediaStreamFilter::AddMediaStream","IMediaStreamFilterAddMediaStream","amstream/IMediaStreamFilter::AddMediaStream","dshow.imediastreamfilter_addmediastream"]
old-location: dshow\imediastreamfilter_addmediastream.htm
tech.root: dshow
ms.assetid: 0e4fdc28-3117-4b9d-a914-ddb70aa5125d
ms.date: 12/05/2018
ms.keywords: AddMediaStream, AddMediaStream method [DirectShow], AddMediaStream method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],AddMediaStream method, IMediaStreamFilter.AddMediaStream, IMediaStreamFilter::AddMediaStream, IMediaStreamFilterAddMediaStream, amstream/IMediaStreamFilter::AddMediaStream, dshow.imediastreamfilter_addmediastream
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
 - IMediaStreamFilter::AddMediaStream
 - amstream/IMediaStreamFilter::AddMediaStream
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
 - IMediaStreamFilter.AddMediaStream
---

# IMediaStreamFilter::AddMediaStream


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>AddMediaStream</code> method connects a media stream object to the underlying filter graph.

## -parameters

### -param pAMMediaStream [in]

Pointer to the media stream object's <a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream</a> interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_PURPOSEID</b></dt>
</dl>
</td>
<td width="60%">
Duplicate purpose ID

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

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>