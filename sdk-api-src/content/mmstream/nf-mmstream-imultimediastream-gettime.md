---
UID: NF:mmstream.IMultiMediaStream.GetTime
title: IMultiMediaStream::GetTime (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetTime method retrieves the current stream time.
helpviewer_keywords: ["GetTime","GetTime method [DirectShow]","GetTime method [DirectShow]","IMultiMediaStream interface","IMultiMediaStream interface [DirectShow]","GetTime method","IMultiMediaStream.GetTime","IMultiMediaStream::GetTime","IMultiMediaStreamGetTime","dshow.imultimediastream_gettime","mmstream/IMultiMediaStream::GetTime"]
old-location: dshow\imultimediastream_gettime.htm
tech.root: dshow
ms.assetid: da92c68b-176c-4773-9ae1-63f803bc206e
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [DirectShow], GetTime method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetTime method, IMultiMediaStream.GetTime, IMultiMediaStream::GetTime, IMultiMediaStreamGetTime, dshow.imultimediastream_gettime, mmstream/IMultiMediaStream::GetTime
req.header: mmstream.h
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
 - IMultiMediaStream::GetTime
 - mmstream/IMultiMediaStream::GetTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMultiMediaStream.GetTime
---

# IMultiMediaStream::GetTime


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <b>GetTime</b> method retrieves the current stream time.

## -parameters

### -param pCurrentTime [out]

Pointer to a variable that receives the stream time, in 100-nanosecond units.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not get the stream time, or there is no clock.

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

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>