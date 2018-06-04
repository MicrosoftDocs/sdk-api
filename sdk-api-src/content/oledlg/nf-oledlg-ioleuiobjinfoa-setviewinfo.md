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

# IOleUIObjInfoA::SetViewInfo


## -description


Sets the view information associated with the object.


## -parameters




### -param dwObject [in]

Unique identifier for the object.


### -param hMetaPict [in]

The new icon.


### -param dvAspect [in]

The new display aspect or view.


### -param nCurrentScale [in]

The new scale.


### -param bRelativeToOrig [in]

The new scale of the object, relative to the origin. This value is <b>TRUE</b> if the scale should be relative to the original scale of the object. If <b>FALSE</b>, <i>nCurrentScale</i> applies to the object's current size.


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
You should apply the new attributes (icon, aspect, and scale) to the object. If <i>bRelativeToOrig</i> is set to <b>TRUE</b>, <i>nCurrentScale</i> (in percentage units) applies to the original size of the object before it was scaled. If <i>bRelativeToOrig</i> is <b>FALSE</b>, <i>nCurrentScale</i> applies to the object's current size.




## -see-also




<a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>



<a href="https://msdn.microsoft.com/508dccb3-e98b-4f62-8bc3-98ca2b0d1349">IOleUIObjInfo</a>
 

 

