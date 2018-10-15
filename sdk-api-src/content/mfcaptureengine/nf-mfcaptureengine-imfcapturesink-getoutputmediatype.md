---
UID: NF:mfcaptureengine.IMFCaptureSink.GetOutputMediaType
title: IMFCaptureSink::GetOutputMediaType
author: windows-sdk-content
description: Gets the output format for a stream on this capture sink.
old-location: mf\imfcapturesink_getoutputmediatype.htm
tech.root: medfound
ms.assetid: 3F050964-9E71-45FC-9553-A2E7A397217E
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetOutputMediaType, GetOutputMediaType method [Media Foundation], GetOutputMediaType method [Media Foundation],IMFCaptureSink interface, IMFCaptureSink interface [Media Foundation],GetOutputMediaType method, IMFCaptureSink.GetOutputMediaType, IMFCaptureSink::GetOutputMediaType, mf.imfcapturesink_getoutputmediatype, mfcaptureengine/IMFCaptureSink::GetOutputMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - mfcaptureengine.h
api_name:
 - IMFCaptureSink.GetOutputMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSink::GetOutputMediaType


## -description


Gets the output format for a stream on this capture sink.


## -parameters




### -param dwSinkStreamIndex [in]

The zero-based index of the stream to query. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a> method.


### -param ppMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the pointer.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSinkStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>
 

 

