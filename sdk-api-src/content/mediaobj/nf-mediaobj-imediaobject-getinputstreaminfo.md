---
UID: NF:mediaobj.IMediaObject.GetInputStreamInfo
title: IMediaObject::GetInputStreamInfo (mediaobj.h)
description: The GetInputStreamInfo method retrieves information about an input stream, such as any restrictions on the number of samples per buffer, and whether the stream performs lookahead on the input data. This information never changes.helpviewer_keywords: ["GetInputStreamInfo","GetInputStreamInfo method [DirectShow]","GetInputStreamInfo method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetInputStreamInfo method","IMediaObject.GetInputStreamInfo","IMediaObject::GetInputStreamInfo","IMediaObjectGetInputStreamInfo","dshow.imediaobject_getinputstreaminfo","mediaobj/IMediaObject::GetInputStreamInfo"]
old-location: dshow\imediaobject_getinputstreaminfo.htm
tech.root: DirectShow
ms.assetid: 9e18bf5e-cf29-4446-a1ba-422b41e02edc
ms.date: 12/05/2018
ms.keywords: GetInputStreamInfo, GetInputStreamInfo method [DirectShow], GetInputStreamInfo method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetInputStreamInfo method, IMediaObject.GetInputStreamInfo, IMediaObject::GetInputStreamInfo, IMediaObjectGetInputStreamInfo, dshow.imediaobject_getinputstreaminfo, mediaobj/IMediaObject::GetInputStreamInfo
f1_keywords:
- mediaobj/IMediaObject.GetInputStreamInfo
dev_langs:
- c++
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
- IMediaObject.GetInputStreamInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaObject::GetInputStreamInfo


## -description



The <code>GetInputStreamInfo</code> method retrieves information about an input stream, such as any restrictions on the number of samples per buffer, and whether the stream performs lookahead on the input data. This information never changes.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of zero or more <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_input_stream_info_flags">DMO_INPUT_STREAM_INFO_FLAGS</a> flags.


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

The application must be sure to allocate sufficient buffers for the DMO to process the input. Call the <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo">IMediaObject::GetInputSizeInfo</a> method to determine the buffer requirements.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>
 

 

