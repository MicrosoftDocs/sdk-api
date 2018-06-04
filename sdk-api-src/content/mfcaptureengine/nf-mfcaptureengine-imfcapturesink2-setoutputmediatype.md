---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

