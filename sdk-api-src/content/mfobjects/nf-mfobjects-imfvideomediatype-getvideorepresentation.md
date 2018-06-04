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

# IMFVideoMediaType::GetVideoRepresentation


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Instead, applications should set the <a href="https://msdn.microsoft.com/71fda231-3497-49db-b82e-2fd79f6ade66">MF_MT_DEFAULT_STRIDE</a> attribute on the media type to specify the surface stride and then call <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">IMFMediaType::GetRepresentation</a>.]


          Retrieves an alternative representation of the media type.


## -parameters




### -param guidRepresentation [in]

GUID that specifies the representation to retrieve. For a list of values, see <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">IMFMediaType::GetRepresentation</a>.


### -param ppvRepresentation [out]

Receives a pointer to a structure that contains the representation. The method allocates the memory for the structure. The caller must release the memory by calling <a href="https://msdn.microsoft.com/d2007f16-543f-4f05-a44d-b4b4ae8019fb">IMFMediaType::FreeRepresentation</a>.


### -param lStride [in]

Stride of the video surface, in bytes. If the stride is unknown, set this value to 0. If the value is 0, the method computes the stride from the image width and assumes that there is no padding.


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
 




## -remarks



This method is equivalent to <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">IMFMediaType::GetRepresentation</a> but includes the <i>lStride</i> parameter.

Instead of calling this method, applications should set the <a href="https://msdn.microsoft.com/71fda231-3497-49db-b82e-2fd79f6ade66">MF_MT_DEFAULT_STRIDE</a> attribute on the media type to specify the surface stride and then call <a href="https://msdn.microsoft.com/2135ff86-a3b6-4e1c-a9de-867f4828f008">IMFMediaType::GetRepresentation</a>.




## -see-also




<a href="https://msdn.microsoft.com/9109b0dd-c44d-41d4-9480-1ca5c667dbd7">IMFVideoMediaType</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

