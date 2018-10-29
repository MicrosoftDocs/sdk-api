---
UID: NF:amstream.IAMMultiMediaStream.GetFilter
title: IAMMultiMediaStream::GetFilter
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetFilter method retrieves the Media Stream filter, which is used internally by the multimedia stream object.
old-location: dshow\iammultimediastream_getfilter.htm
tech.root: DirectShow
ms.assetid: 7e4df9cb-4008-4615-a179-ae1e76c22337
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetFilter, GetFilter method [DirectShow], GetFilter method [DirectShow],IAMMultiMediaStream interface, IAMMultiMediaStream interface [DirectShow],GetFilter method, IAMMultiMediaStream.GetFilter, IAMMultiMediaStream::GetFilter, IAMMultiMediaStreamGetFilter, amstream/IAMMultiMediaStream::GetFilter, dshow.iammultimediastream_getfilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMultiMediaStream.GetFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMultiMediaStream::GetFilter


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFilter</code> method retrieves the Media Stream filter, which is used internally by the multimedia stream object.




## -parameters




### -param ppFilter [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/1ac4976b-7088-47ac-9689-58c143746f05">IMediaStreamFilter</a> interface pointer.


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



Applications should not call this method. The <b>IMediaStreamFilter</b> interface is not intended for applications to use.

If the method succeeds, the caller must release the <b>IMediaStreamFilter</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/2f604156-68ef-4770-9929-6dbfd46c4d6d">IAMMultiMediaStream Interface</a>
 

 

