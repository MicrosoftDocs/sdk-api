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

# ICallFrame::Unmarshal


## -description


Unmarshals a packet of data containing the previously marshaled [out] parameters of a call into this already existing activation record.


## -parameters




### -param pBuffer [in]

A pointer to the buffer containing the marshaled [out] values.


### -param cbBuffer [in]

The size of the buffer, in bytes.


### -param dataRep [in]

The NDR data representation with which the data was marshaled. For more information, see <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">IRpcChannelBuffer::GetBuffer</a>.


### -param pcontext [in]

A pointer to the <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how unmarshalling is carried out.


### -param pcbUnmarshalled [out]

Receives the number of bytes that were successfully unmarshaled. This parameter is returned even in error situations. This parameter is optional.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



When unmarshalling, the [in] versions of [in, out] parameters are freed and interface pointers are released and replaced with there [out] versions. All the [in, out] and [out] parameters will always be set to reasonable [in], [in, out] values, [out] values successfully unmarshaled from the returned data, or a value explicitly initialized to <b>NULL</b>. On failure return, the caller will typically want to call <a href="https://msdn.microsoft.com/97261d93-40cf-4a27-9bee-677600c04699">ICallFrame::Free</a> in order to clean up the values that are not <b>NULL</b>.






## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

