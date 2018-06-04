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

# IOleUIObjInfoA::GetConvertInfo


## -description


Gets the conversion information associated with the specified object.


## -parameters




### -param dwObject [in]

Unique identifier for the object.


### -param lpClassID [out]

Pointer to the location to return the object's CLSID.


### -param lpwFormat [out]

Pointer to the clipboard format of the object.


### -param lpConvertDefaultClassID [out]

Pointer to the default class, selected from the UI, to convert the object to.


### -param lplpClsidExclude [out]

Address of a pointer variable that receives a pointer to an array of CLSIDs that should be excluded from the user interface for this object. If <i>lpcClsidExclude</i> is zero, then <i>lpClsidExclude</i> is set to <b>NULL</b>.


### -param lpcClsidExclude [out]

Address of an output variable that receives the number of CLSIDs in <i>lplpClsidExclude</i>. This parameter may be zero.


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
The specified identifier is invalid.

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
You must fill in the CLSID of the object at a minimum. <i>lpwFormat</i> may be left at zero if the format of the storage is unknown.




## -see-also




<a href="https://msdn.microsoft.com/508dccb3-e98b-4f62-8bc3-98ca2b0d1349">IOleUIObjInfo</a>
 

 

