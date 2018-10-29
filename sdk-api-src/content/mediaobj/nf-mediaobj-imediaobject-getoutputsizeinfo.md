---
UID: NF:mediaobj.IMediaObject.GetOutputSizeInfo
title: IMediaObject::GetOutputSizeInfo
author: windows-sdk-content
description: The GetOutputSizeInfo method retrieves the buffer requirements for a specified output stream.
old-location: dshow\imediaobject_getoutputsizeinfo.htm
tech.root: DirectShow
ms.assetid: 497bc88e-4e26-409f-9d42-6a214a5d56e9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetOutputSizeInfo, GetOutputSizeInfo method [DirectShow], GetOutputSizeInfo method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetOutputSizeInfo method, IMediaObject.GetOutputSizeInfo, IMediaObject::GetOutputSizeInfo, IMediaObjectGetOutputSizeInfo, dshow.imediaobject_getoutputsizeinfo, mediaobj/IMediaObject::GetOutputSizeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMediaObject.GetOutputSizeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObject::GetOutputSizeInfo


## -description



The <code>GetOutputSizeInfo</code> method retrieves the buffer requirements for a specified output stream.




## -parameters




### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pcbSize [out]

Pointer to a variable that receives the minimum size of an output buffer for this stream, in bytes.


### -param pcbAlignment [out]

Pointer to a variable that receives the required buffer alignment, in bytes. If the output stream has no alignment requirement, the value is 1.


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



The buffer requirements may depend on the media types set for each of the streams.

Before calling this method, set the media type of each stream by calling the <a href="https://msdn.microsoft.com/6b466fe4-97a0-46f9-9e4b-461ee66095f1">IMediaObject::SetInputType</a> and <a href="https://msdn.microsoft.com/1dda3c55-d37b-4e04-9509-0e5197d6b019">IMediaObject::SetOutputType</a> methods. If the media types have not been set, this method might return an error. However, if a stream is optional, and the application will not use the stream, you do not have to set the media type for the stream.

A buffer is <i>aligned</i> if the buffer's start address is a multiple of <i>*pcbAlignment</i>. Depending on the architecture of the microprocessor, it is faster to read and write to an aligned buffer than to an unaligned buffer. On some microprocessors, reading and writing to an unaligned buffer is not supported and can cause the program to crash. Zero is not a valid alignment.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

