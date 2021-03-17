---
UID: NF:amstream.IMediaStreamFilter.EnumMediaStreams
title: IMediaStreamFilter::EnumMediaStreams (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The EnumMediaStreams method retrieves a media stream, specified by index.
helpviewer_keywords: ["EnumMediaStreams","EnumMediaStreams method [DirectShow]","EnumMediaStreams method [DirectShow]","IMediaStreamFilter interface","IMediaStreamFilter interface [DirectShow]","EnumMediaStreams method","IMediaStreamFilter.EnumMediaStreams","IMediaStreamFilter::EnumMediaStreams","IMediaStreamFilterEnumMediaStreams","amstream/IMediaStreamFilter::EnumMediaStreams","dshow.imediastreamfilter_enummediastreams"]
old-location: dshow\imediastreamfilter_enummediastreams.htm
tech.root: dshow
ms.assetid: 5f62abda-6192-4adb-985d-9bffe310b407
ms.date: 12/05/2018
ms.keywords: EnumMediaStreams, EnumMediaStreams method [DirectShow], EnumMediaStreams method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],EnumMediaStreams method, IMediaStreamFilter.EnumMediaStreams, IMediaStreamFilter::EnumMediaStreams, IMediaStreamFilterEnumMediaStreams, amstream/IMediaStreamFilter::EnumMediaStreams, dshow.imediastreamfilter_enummediastreams
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
 - IMediaStreamFilter::EnumMediaStreams
 - amstream/IMediaStreamFilter::EnumMediaStreams
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
 - IMediaStreamFilter.EnumMediaStreams
---

# IMediaStreamFilter::EnumMediaStreams


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>EnumMediaStreams</code> method retrieves a media stream, specified by index.

## -parameters

### -param Index [in]

Index of the media stream to retrieve.

### -param ppMediaStream [out]

Address of a variable that receives an <a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> interface pointer.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

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

If the method succeeds, the caller must release the <b>IMediaStream</b> interface.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-imediastreamfilter">IMediaStreamFilter Interface</a>