---
UID: NF:mfreadwrite.IMFSinkWriter.SetInputMediaType
title: IMFSinkWriter::SetInputMediaType
author: windows-driver-content
description: Sets the input format for a stream on the sink writer.
old-location: mf\imfsinkwriter_setinputmediatype.htm
old-project: medfound
ms.assetid: 02a73f73-3b25-4578-9a7e-c9f8a4c8cd99
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],SetInputMediaType method, IMFSinkWriter.SetInputMediaType, IMFSinkWriter::SetInputMediaType, SetInputMediaType, SetInputMediaType method [Media Foundation], SetInputMediaType method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_setinputmediatype, mfreadwrite/IMFSinkWriter::SetInputMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSinkWriter.SetInputMediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSinkWriter::SetInputMediaType


## -description


Sets the input format for a stream on the sink writer.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. The index is received by the <i>pdwStreamIndex</i> parameter of the <a href="https://msdn.microsoft.com/9f9b1216-e915-4188-bcfd-6c41e1821ec4">IMFSinkWriter::AddStream</a> method.


### -param pInputMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a media type. The media type specifies the input format.


### -param pEncodingParameters [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store. Use the attribute store to configure the encoder. This parameter can be <b>NULL</b>.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDMEDIATYPE</b></b></dt>
</dl>
</td>
<td width="60%">
The underlying media sink does not support the format, no conversion is possible, or a dynamic format change is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDSTREAMNUMBER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>dwStreamIndex</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_TOPO_CODEC_NOT_FOUND</b></b></dt>
</dl>
</td>
<td width="60%">
Could not find an encoder for the encoded format.

</td>
</tr>
</table>
 




## -remarks



The input format does not have to match the target format that is written to the media sink. If the formats do not match, the method attempts to load an encoder that can encode from the input format to the target format.

After streaming begins—that is, after the  first call to <a href="https://msdn.microsoft.com/1c65a5d0-cc1b-456e-9d88-a24da57ee30a">IMFSinkWriter::WriteSample</a>—you can call this method at any time to change the input format.  However, the underlying encoder and media sink must support dynamic format changes.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

