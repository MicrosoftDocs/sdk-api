---
UID: NF:mmstream.IMultiMediaStream.GetEndOfStreamEventHandle
title: IMultiMediaStream::GetEndOfStreamEventHandle
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetEndOfStreamEventHandle method retrieves an event that is signaled when the multimedia stream completes playback.
old-location: dshow\imultimediastream_getendofstreameventhandle.htm
tech.root: DirectShow
ms.assetid: 0e4f59f8-c56e-4768-9047-2793515edfeb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetEndOfStreamEventHandle, GetEndOfStreamEventHandle method [DirectShow], GetEndOfStreamEventHandle method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetEndOfStreamEventHandle method, IMultiMediaStream.GetEndOfStreamEventHandle, IMultiMediaStream::GetEndOfStreamEventHandle, IMultiMediaStreamGetEndOfStreamEventHandle, dshow.imultimediastream_getendofstreameventhandle, mmstream/IMultiMediaStream::GetEndOfStreamEventHandle
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMultiMediaStream.GetEndOfStreamEventHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmstream.h
: 
- IMultiMediaStream.GetEndOfStreamEventHandle
: 
---

# IMultiMediaStream::GetEndOfStreamEventHandle


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetEndOfStreamEventHandle</code> method retrieves an event that is signaled when the multimedia stream completes playback.




## -parameters




### -param phEOS [out]

Pointer to a variable that receives a handle to the event. The event is signaled when all of the streams in the multimedia stream object complete playback.


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
<dt><b>MS_E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The multimedia stream is not stopped.

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




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

