---
UID: NF:mediaobj.IMediaObject.GetInputStreamInfo
title: IMediaObject::GetInputStreamInfo
author: windows-sdk-content
description: The GetInputStreamInfo method retrieves information about an input stream, such as any restrictions on the number of samples per buffer, and whether the stream performs lookahead on the input data. This information never changes.
old-location: dshow\imediaobject_getinputstreaminfo.htm
old-project: DirectShow
ms.assetid: 9e18bf5e-cf29-4446-a1ba-422b41e02edc
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetInputStreamInfo, GetInputStreamInfo method [DirectShow], GetInputStreamInfo method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputStreamInfo method, IMediaObject.GetInputStreamInfo, IMediaObject::GetInputStreamInfo, IMediaObjectGetInputStreamInfo, dshow.imediaobject_getinputstreaminfo, mediaobj/IMediaObject::GetInputStreamInfo
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
 - IMediaObject.GetInputStreamInfo
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::GetInputStreamInfo


## -description



The <code>GetInputStreamInfo</code> method retrieves information about an input stream, such as any restrictions on the number of samples per buffer, and whether the stream performs lookahead on the input data. This information never changes.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of zero or more <a href="https://msdn.microsoft.com/96e37678-0325-4569-8491-c8ef23f6c76e">DMO_INPUT_STREAM_INFO_FLAGS</a> flags.


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
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



The DMO_INPUT_STREAMF_HOLDS_BUFFERS flag indicates that the DMO performs lookahead on the incoming data.

The application must be sure to allocate sufficient buffers for the DMO to process the input. Call the <a href="https://msdn.microsoft.com/cce6359a-cd6e-46c9-a1cb-553ae5f83b9c">IMediaObject::GetInputSizeInfo</a> method to determine the buffer requirements.




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

