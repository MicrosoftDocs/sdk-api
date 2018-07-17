---
UID: NF:mediaobj.IMediaObject.GetInputSizeInfo
title: IMediaObject::GetInputSizeInfo
author: windows-sdk-content
description: The GetInputSizeInfo method retrieves the buffer requirements for a specified input stream.
old-location: dshow\imediaobject_getinputsizeinfo.htm
old-project: DirectShow
ms.assetid: cce6359a-cd6e-46c9-a1cb-553ae5f83b9c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetInputSizeInfo, GetInputSizeInfo method [DirectShow], GetInputSizeInfo method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputSizeInfo method, IMediaObject.GetInputSizeInfo, IMediaObject::GetInputSizeInfo, IMediaObjectGetInputSizeInfo, dshow.imediaobject_getinputsizeinfo, mediaobj/IMediaObject::GetInputSizeInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.GetInputSizeInfo
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::GetInputSizeInfo


## -description



The <code>GetInputSizeInfo</code> method retrieves the buffer requirements for a specified input stream.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param pcbSize [out]

Pointer to a variable that receives the minimum size of an input buffer for this stream, in bytes.


### -param pcbMaxLookahead [out]

Pointer to a variable that receives the maximum amount of data that the DMO will hold for lookahead, in bytes. If the DMO does not perform lookahead on the stream, the value is zero.


### -param pcbAlignment [out]

Pointer to a variable that receives the required buffer alignment, in bytes. If the input stream has no alignment requirement, the value is 1.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The buffer requirements may depend on the media types of the various streams. Before calling this method, set the media type of each stream by calling the <a href="https://msdn.microsoft.com/6b466fe4-97a0-46f9-9e4b-461ee66095f1">IMediaObject::SetInputType</a> and <a href="https://msdn.microsoft.com/1dda3c55-d37b-4e04-9509-0e5197d6b019">IMediaObject::SetOutputType</a> methods. If the media types have not been set, this method might return an error.

If the DMO performs lookahead on the input stream, it returns the DMO_INPUT_STREAMF_HOLDS_BUFFERS flag in the <a href="https://msdn.microsoft.com/9e18bf5e-cf29-4446-a1ba-422b41e02edc">IMediaObject::GetInputStreamInfo</a> method. During processing, the DMO holds up to the number of bytes indicated by the <i>pcbMaxLookahead</i> parameter. The application must allocate enough buffers for the DMO to hold this much data.

A buffer is <i>aligned</i> if the buffer's start address is a multiple of <i>*pcbAlignment</i>. The alignment must be a power of two. Depending on the microprocessor, reads and writes to an aligned buffer might be faster than to an unaligned buffer. Also, some microprocessors do not support unaligned reads and writes.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

