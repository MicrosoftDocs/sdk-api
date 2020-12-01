---
UID: NF:amstream.IMediaStreamFilter.GetMediaStream
title: IMediaStreamFilter::GetMediaStream (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetMediaStream method retrieves a media stream, specified by purpose ID.
helpviewer_keywords: ["GetMediaStream","GetMediaStream method [DirectShow]","GetMediaStream method [DirectShow]","IMediaStreamFilter interface","IMediaStreamFilter interface [DirectShow]","GetMediaStream method","IMediaStreamFilter.GetMediaStream","IMediaStreamFilter::GetMediaStream","IMediaStreamFilterGetMediaStream","amstream/IMediaStreamFilter::GetMediaStream","dshow.imediastreamfilter_getmediastream"]
old-location: dshow\imediastreamfilter_getmediastream.htm
tech.root: dshow
ms.assetid: 27ef63cf-36a4-4d35-bd38-3c51b1343ee1
ms.date: 12/05/2018
ms.keywords: GetMediaStream, GetMediaStream method [DirectShow], GetMediaStream method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],GetMediaStream method, IMediaStreamFilter.GetMediaStream, IMediaStreamFilter::GetMediaStream, IMediaStreamFilterGetMediaStream, amstream/IMediaStreamFilter::GetMediaStream, dshow.imediastreamfilter_getmediastream
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
 - IMediaStreamFilter::GetMediaStream
 - amstream/IMediaStreamFilter::GetMediaStream
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
 - IMediaStreamFilter.GetMediaStream
---

# IMediaStreamFilter::GetMediaStream


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaStream</code> method retrieves a media stream, specified by purpose ID.

## -parameters

### -param idPurpose [in]

Reference to an <a href="/windows/desktop/DirectShow/mspid">MSPID</a> value that specifies which stream to retrieve.

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
<dt><b>MS_E_NOSTREAM</b></dt>
</dl>
</td>
<td width="60%">
No matching stream was found.

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