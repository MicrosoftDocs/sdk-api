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

# IWMMediaProps::GetType


## -description



The <b>GetType</b> method retrieves the major type of the media in the stream, input, or output described by the object to which the current <b>IWMMediaProps</b> interface belongs.




## -parameters




### -param pguidType [out]

Pointer to a GUID specifying the media type.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pguidType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



These media types are used by the writer, reader, and profile objects to identify the properties of a media stream that are specific to the media type.

<b>GetType</b> is provided for convenience; it returns the same value as the <b>majortype</b> member of <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a>.




## -see-also




<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps Interface</a>



<a href="https://msdn.microsoft.com/8357e5c6-d8c6-4a30-8446-85fa7fa118f7">IWMMediaProps::GetMediaType</a>



<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>



<a href="https://msdn.microsoft.com/00dcbb20-09ed-44c5-992c-20f3d17ad47c">Media Types</a>
 

 

