---
UID: NF:mfreadwrite.IMFSinkWriter.SetInputMediaType
title: IMFSinkWriter::SetInputMediaType (mfreadwrite.h)
description: Sets the input format for a stream on the sink writer.
helpviewer_keywords: ["IMFSinkWriter interface [Media Foundation]","SetInputMediaType method","IMFSinkWriter.SetInputMediaType","IMFSinkWriter::SetInputMediaType","SetInputMediaType","SetInputMediaType method [Media Foundation]","SetInputMediaType method [Media Foundation]","IMFSinkWriter interface","mf.imfsinkwriter_setinputmediatype","mfreadwrite/IMFSinkWriter::SetInputMediaType"]
old-location: mf\imfsinkwriter_setinputmediatype.htm
tech.root: mf
ms.assetid: 02a73f73-3b25-4578-9a7e-c9f8a4c8cd99
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],SetInputMediaType method, IMFSinkWriter.SetInputMediaType, IMFSinkWriter::SetInputMediaType, SetInputMediaType, SetInputMediaType method [Media Foundation], SetInputMediaType method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_setinputmediatype, mfreadwrite/IMFSinkWriter::SetInputMediaType
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSinkWriter::SetInputMediaType
 - mfreadwrite/IMFSinkWriter::SetInputMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriter.SetInputMediaType
---

# IMFSinkWriter::SetInputMediaType


## -description

Sets the input format for a stream on the sink writer.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of the stream. The index is received by the <i>pdwStreamIndex</i> parameter of the <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream">IMFSinkWriter::AddStream</a> method.

### -param pInputMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a media type. The media type specifies the input format.

### -param pEncodingParameters [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store. Use the attribute store to configure the encoder. This parameter can be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The underlying media sink does not support the format, no conversion is possible, or a dynamic format change is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwStreamIndex</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TOPO_CODEC_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find an encoder for the encoded format.

</td>
</tr>
</table>

## -remarks

The input format does not have to match the target format that is written to the media sink. If the formats do not match, the method attempts to load an encoder that can encode from the input format to the target format.

After streaming begins—that is, after the  first call to <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample">IMFSinkWriter::WriteSample</a>—you can call this method at any time to change the input format.  However, the underlying encoder and media sink must support dynamic format changes.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>