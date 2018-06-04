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

# IMFASFProfile::GetStream


## -description



Retrieves a stream from the profile by stream index, and/or retrieves the stream number for a stream index.




## -parameters




### -param dwStreamIndex [in]

The index of the stream to retrieve. Stream indexes are sequential and zero-based. You can get the number of streams that are in the profile by calling the <a href="https://msdn.microsoft.com/bf8c6157-3420-4097-8ab6-f307a69d418a">IMFASFProfile::GetStreamCount</a> method.


### -param pwStreamNumber [out]

Receives the stream number of the requested stream. Stream numbers are one-based and are not necessarily sequential. This parameter can be set to <b>NULL</b> if the stream number is not required.


### -param ppIStream [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a> interface of the ASF stream configuration object. The caller must release the interface. This parameter can be <b>NULL</b> if you want to retrieve the stream number without accessing the stream configuration.


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



This method does not create a copy of the stream configuration object. The pointer that is retrieved points to the object within the profile object. You must not make any changes to the stream configuration object using this pointer, because doing so can affect the profile object in unexpected ways.

To change the configuration of the stream configuration object in the profile, you must first clone the stream configuration object by calling <a href="https://msdn.microsoft.com/c87d658f-6569-464b-a9d0-487d44f76cc0">IMFASFStreamConfig::Clone</a>. Make whatever changes are required to the clone of the object and then add the updated object by calling the <a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a> method.




## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/fe441c61-1be7-4fda-a2a3-bd79ecf4e54c">IMFASFProfile</a>



<a href="https://msdn.microsoft.com/1e3fadf0-1549-4d51-b263-727b15c55023">IMFASFProfile::GetStreamByNumber</a>



<a href="https://msdn.microsoft.com/bf8c6157-3420-4097-8ab6-f307a69d418a">IMFASFProfile::GetStreamCount</a>



<a href="https://msdn.microsoft.com/dfe404d3-66ea-407b-a2e0-caa065f41afe">IMFASFProfile::RemoveStream</a>



<a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">IMFASFProfile::SetStream</a>



<a href="https://msdn.microsoft.com/7bb63396-21c2-400d-b9de-c00b90f46d62">IMFASFStreamConfig</a>
 

 

