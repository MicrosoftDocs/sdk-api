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

# IOleUIObjInfoA::GetViewInfo


## -description


Gets the view information associated with the object.


## -parameters




### -param dwObject [in]

Unique  identifier for the object.


### -param phMetaPict [in, optional]

Pointer to the object's current icon. This parameter can be <b>NULL</b>, indicating that the caller is not interested in the object's current presentation.


### -param pdvAspect [in, optional]

Pointer to the object's current aspect. This parameter can be <b>NULL</b>, indicating that the caller is not interested in the object's current aspect, for example, DVASPECT_ICONIC or DVASPECT_CONTENT.


### -param pnCurrentScale [in, optional]

Pointer to the object's current scale. This parameter can be <b>NULL</b>, indicating that the caller is not interested in the current scaling factor applied to the object in the container's view.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Insufficient access permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You must fill in the object's current icon, aspect, and scale.




## -see-also




<a href="https://msdn.microsoft.com/508dccb3-e98b-4f62-8bc3-98ca2b0d1349">IOleUIObjInfo</a>



<a href="https://msdn.microsoft.com/e45565c5-185e-4143-a5c2-d0b273b5086e">OLEUIVIEWPROPS</a>
 

 

