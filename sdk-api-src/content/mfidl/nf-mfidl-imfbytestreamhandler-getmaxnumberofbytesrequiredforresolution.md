---
UID: NF:mfidl.IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution
title: IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution (mfidl.h)
description: Retrieves the maximum number of bytes needed to create the media source or determine that the byte stream handler cannot parse this stream.
helpviewer_keywords: ["GetMaxNumberOfBytesRequiredForResolution","GetMaxNumberOfBytesRequiredForResolution method [Media Foundation]","GetMaxNumberOfBytesRequiredForResolution method [Media Foundation]","IMFByteStreamHandler interface","IMFByteStreamHandler interface [Media Foundation]","GetMaxNumberOfBytesRequiredForResolution method","IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution","IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution","e90c5bc6-fc0a-4478-aa65-9dc6618f46f0","mf.imfbytestreamhandler_getmaxnumberofbytesrequiredforresolution","mfidl/IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution"]
old-location: mf\imfbytestreamhandler_getmaxnumberofbytesrequiredforresolution.htm
tech.root: mf
ms.assetid: e90c5bc6-fc0a-4478-aa65-9dc6618f46f0
ms.date: 12/05/2018
ms.keywords: GetMaxNumberOfBytesRequiredForResolution, GetMaxNumberOfBytesRequiredForResolution method [Media Foundation], GetMaxNumberOfBytesRequiredForResolution method [Media Foundation],IMFByteStreamHandler interface, IMFByteStreamHandler interface [Media Foundation],GetMaxNumberOfBytesRequiredForResolution method, IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution, IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution, e90c5bc6-fc0a-4478-aa65-9dc6618f46f0, mf.imfbytestreamhandler_getmaxnumberofbytesrequiredforresolution, mfidl/IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution
 - mfidl/IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStreamHandler.GetMaxNumberOfBytesRequiredForResolution
---

# IMFByteStreamHandler::GetMaxNumberOfBytesRequiredForResolution


## -description

Retrieves the maximum number of bytes needed to create the media source or determine that the byte stream handler cannot parse this stream.

## -parameters

### -param pqwBytes [out]

Receives the maximum number of bytes that are required.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler">IMFByteStreamHandler</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>