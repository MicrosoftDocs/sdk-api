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

# IWMMediaProps::GetMediaType


## -description



The <b>GetMediaType</b> method retrieves a structure describing the media type.




## -parameters




### -param pType [out]

Pointer to a <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a> structure. If this parameter is set to <b>NULL</b>, this method returns the size of the buffer required in the <i>pcbType</i> parameter.


### -param pcbType [in, out]

On input, the size of the <i>pType</i> buffer. On output, if <i>pType</i> is set to <b>NULL</b>, the value this points to is set to the size of the buffer needed to hold the media type structure.


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
The <i>pcbType</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcbType</i> parameter is not large enough.

</td>
</tr>
</table>
 




## -remarks



You must make two calls to <b>GetMediaType</b>. On the first call, pass <b>NULL</b> as <i>pType</i>. On return, the value of <i>pcbType</i> will be set to the buffer size required to hold the <b>WM_MEDIA_TYPE</b> structure. Then you can allocate a buffer of the required size and pass a pointer to it as <i>pType</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/a81abd80-e487-421c-ba81-9b43c4233084">IWMMediaProps Interface</a>



<a href="https://msdn.microsoft.com/7a89bf24-6b76-4645-8f39-f1979029d67e">IWMMediaProps::SetMediaType</a>



<a href="https://msdn.microsoft.com/00dcbb20-09ed-44c5-992c-20f3d17ad47c">Media Types</a>
 

 

