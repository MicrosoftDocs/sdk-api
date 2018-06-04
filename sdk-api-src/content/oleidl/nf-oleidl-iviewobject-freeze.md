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

# IViewObject::Freeze


## -description


Freezes the drawn representation of an object so that it will not change until the <a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">IViewObject::Unfreeze</a> method is called. The most common use of this method is for banded printing.


## -parameters




### -param dwDrawAspect [in]

Specifies how the object is to be represented. Representations include content, an icon, a thumbnail, or a printed document. Valid values are taken from the enumeration <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>. See the <b>DVASPECT</b> enumeration for more information.


### -param lindex [in]

Portion of the object that is of interest for the draw operation. Its interpretation varies with dwAspect. See the <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> enumeration for more information.


### -param pvAspect [in]

Pointer to additional information about the view of the object specified in <i>dwAspect</i>. Since none of the current aspects support additional information, <i>pvAspect</i> must always be <b>NULL</b>.


### -param pdwFreeze [out]

Pointer to where an identifying DWORD key is returned. This unique key is later used to cancel the freeze by calling <a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">IViewObject::Unfreeze</a>. This key is an index that the default cache uses to keep track of which object is frozen.


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
<dt><b>VIEW_S_ALREADY_FROZEN</b></dt>
</dl>
</td>
<td width="60%">
Presentation has already been frozen. The value of <i>pdwFreeze</i> is the identifying key of the already frozen object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
Presentation not in cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>lindex</i>; currently; only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>dwAspect</i>.

</td>
</tr>
</table>
 




## -remarks



The <b>IViewObject::Freeze</b> method causes the view object to freeze its drawn representation until a subsequent call to <a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">IViewObject::Unfreeze</a> releases it. After calling <b>IViewObject::Freeze</b>, successive calls to <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a> with the same parameters produce the same picture until <b>IViewObject::Unfreeze</b> is called.

<b>IViewObject::Freeze</b> is not part of the persistent state of the object and does not continue across unloads and reloads of the object.

The most common use of this method is for banded printing.

While in a frozen state, view notifications are not sent. Pending view notifications are deferred to the subsequent call to <a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">IViewObject::Unfreeze</a>.




## -see-also




<a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a>



<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>



<a href="https://msdn.microsoft.com/76f3c5f6-3f29-4a89-94e2-f77489e6a744">IViewObject::Unfreeze</a>
 

 

