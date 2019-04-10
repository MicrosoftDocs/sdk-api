---
UID: NF:mediaobj.IMediaObject.GetInputCurrentType
title: IMediaObject::GetInputCurrentType (mediaobj.h)
author: windows-sdk-content
description: The GetInputCurrentType method retrieves the media type that was set for an input stream, if any.
old-location: dshow\imediaobject_getinputcurrenttype.htm
tech.root: DirectShow
ms.assetid: 81d5c1b8-086c-422d-b2d7-85728507888d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInputCurrentType, GetInputCurrentType method [DirectShow], GetInputCurrentType method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputCurrentType method, IMediaObject.GetInputCurrentType, IMediaObject::GetInputCurrentType, IMediaObjectGetInputCurrentType, dshow.imediaobject_getinputcurrenttype, mediaobj/IMediaObject::GetInputCurrentType
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.GetInputCurrentType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObject::GetInputCurrentType


## -description



The <code>GetInputCurrentType</code> method retrieves the media type that was set for an input stream, if any.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param pmt [out]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd375504(v=VS.85).aspx">DMO_MEDIA_TYPE</a> structure allocated by the caller. The method fills the structure with the media type.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
Media type was not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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



The caller must set the media type for the stream before calling this method. To set the media type, call the <a href="https://msdn.microsoft.com/en-us/library/Dd406962(v=VS.85).aspx">IMediaObject::SetInputType</a> method.

If the method succeeds, call <a href="https://msdn.microsoft.com/en-us/library/Dd390698(v=VS.85).aspx">MoFreeMediaType</a> to free the format block.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd406926(v=VS.85).aspx">IMediaObject Interface</a>
 

 

