---
UID: NF:mmstream.IMultiMediaStream.EnumMediaStreams
title: IMultiMediaStream::EnumMediaStreams
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The EnumMediaStreams method retrieves a media stream object, specified by index.
old-location: dshow\imultimediastream_enummediastreams.htm
tech.root: DirectShow
ms.assetid: 2fb51794-83ac-44c5-b388-d7b945870324
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumMediaStreams, EnumMediaStreams method [DirectShow], EnumMediaStreams method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],EnumMediaStreams method, IMultiMediaStream.EnumMediaStreams, IMultiMediaStream::EnumMediaStreams, IMultiMediaStreamEnumMediaStreams, dshow.imultimediastream_enummediastreams, mmstream/IMultiMediaStream::EnumMediaStreams
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
 - IMultiMediaStream.EnumMediaStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMultiMediaStream::EnumMediaStreams


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>EnumMediaStreams</code> method retrieves a media stream object, specified by index.




## -parameters




### -param Index [in]

Zero-based index of the media stream to retrieve.


### -param ppMediaStream [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> interface pointer.


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
Index is out of range.

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



If the return value is S_OK, the caller must release the <b>IMediaStream</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

