---
UID: NF:mmstream.IMultiMediaStream.Seek
title: IMultiMediaStream::Seek (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. The Seek method seeks all of the media streams to a new position.
helpviewer_keywords: ["IMultiMediaStream interface [DirectShow]","Seek method","IMultiMediaStream.Seek","IMultiMediaStream::Seek","IMultiMediaStreamSeek","Seek","Seek method [DirectShow]","Seek method [DirectShow]","IMultiMediaStream interface","dshow.imultimediastream_seek","mmstream/IMultiMediaStream::Seek"]
old-location: dshow\imultimediastream_seek.htm
tech.root: DirectShow
ms.assetid: ac65613f-3fca-4043-83ad-740ebd7687a4
ms.date: 12/05/2018
ms.keywords: IMultiMediaStream interface [DirectShow],Seek method, IMultiMediaStream.Seek, IMultiMediaStream::Seek, IMultiMediaStreamSeek, Seek, Seek method [DirectShow], Seek method [DirectShow],IMultiMediaStream interface, dshow.imultimediastream_seek, mmstream/IMultiMediaStream::Seek
f1_keywords:
- mmstream/IMultiMediaStream.Seek
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mmstream.h
api_name:
- IMultiMediaStream.Seek
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultiMediaStream::Seek


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Seek</code> method seeks all of the media streams to a new position.




## -parameters




### -param SeekTime [in]


<a href="https://docs.microsoft.com/windows/desktop/DirectShow/stream-time">STREAM_TIME</a> value that specifies the new position.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The media streams do not support seeking.

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



To determine whether the media streams support seeking, call the <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getinformation">IMultiMediaStream::GetInformation</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream Interface</a>
 

 

