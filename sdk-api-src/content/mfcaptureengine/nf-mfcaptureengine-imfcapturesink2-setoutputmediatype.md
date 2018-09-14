---
UID: NF:mfcaptureengine.IMFCaptureSink2.SetOutputMediaType
title: IMFCaptureSink2::SetOutputMediaType
author: windows-sdk-content
description: Dynamically sets the output media type of the record sink or preview sink.
old-location: mf\imfcapturesink2_setoutputmediatype.htm
tech.root: medfound
ms.assetid: e9a653c3-927b-4577-9a54-2d63f6b29c06
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFCaptureSink2 interface [Media Foundation],SetOutputMediaType method, IMFCaptureSink2.SetOutputMediaType, IMFCaptureSink2::SetOutputMediaType, SetOutputMediaType, SetOutputMediaType method [Media Foundation], SetOutputMediaType method [Media Foundation],IMFCaptureSink2 interface, mf.imfcapturesink2_setoutputmediatype, mfcaptureengine/IMFCaptureSink2::SetOutputMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfcaptureengine.idl
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
 - IMFCaptureSink2.SetOutputMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSink2::SetOutputMediaType


## -description


Dynamically sets the output media type of the record sink or preview sink.


## -parameters




### -param dwStreamIndex [in]

The stream index to change the output media type on.


### -param pMediaType [in]

The new output media type.


### -param pEncodingAttributes [in]

The new encoder attributes. This can be  <b>null</b>.


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
The method succeeded

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALID_MEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The sink does not support the media type.

</td>
</tr>
</table>
 




## -remarks



This is an asynchronous call.  Listen to the <a href="https://msdn.microsoft.com/A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC">MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET</a> event
to be notified when the output media type has been set.




## -see-also




<a href="https://msdn.microsoft.com/afaf0d2e-3732-4c78-8aba-870c6aaefa28">IMFCaptureSink2</a>
 

 

