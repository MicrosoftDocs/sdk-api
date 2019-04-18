---
UID: NF:mmstream.IMultiMediaStream.GetMediaStream
title: IMultiMediaStream::GetMediaStream (mmstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetMediaStream method retrieves a media stream, specified by purpose ID.
old-location: dshow\imultimediastream_getmediastream.htm
tech.root: DirectShow
ms.assetid: d85cde4f-99f4-4641-b75f-13ca6dc7f21e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMediaStream, GetMediaStream method [DirectShow], GetMediaStream method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetMediaStream method, IMultiMediaStream.GetMediaStream, IMultiMediaStream::GetMediaStream, IMultiMediaStreamGetMediaStream, dshow.imultimediastream_getmediastream, mmstream/IMultiMediaStream::GetMediaStream
ms.topic: method
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
 - IMultiMediaStream.GetMediaStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultiMediaStream::GetMediaStream


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaStream</code> method retrieves a media stream, specified by purpose ID.




## -parameters




### -param idPurpose

Reference to an <a href="https://msdn.microsoft.com/83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf">MSPID</a> that identifies the media stream to retrieve.


### -param ppMediaStream

Address of variable that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd407041(v=VS.85).aspx">IMediaStream</a> interface pointer.


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
<b>NULL</b> pointer valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_NOSTREAM</b></dt>
</dl>
</td>
<td width="60%">
No matching stream.

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




<a href="https://msdn.microsoft.com/en-us/library/Dd390325(v=VS.85).aspx">IMultiMediaStream Interface</a>
 

 

