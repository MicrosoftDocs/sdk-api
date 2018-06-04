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

# CoGetTreatAsClass function


## -description


Returns the CLSID of an object that can emulate the specified object.




## -parameters




### -param clsidOld [in]

The CLSID of the object that can be emulated (treated as) an object with a different CLSID.


### -param pClsidNew [out]

A pointer to where the CLSID that can emulate <i>clsidOld</i> objects is retrieved. This parameter cannot be <b>NULL</b>. If there is no emulation information for <i>clsidOld</i> objects, the <i>clsidOld</i> parameter is supplied.


## -returns



This function can return the following values, as well as any error values returned by the <a href="https://msdn.microsoft.com/36cc9037-480f-491f-a9bb-5aa1e707781e">CLSIDFromString</a> function.

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
A new CLSID was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no emulation information for the <i>clsidOld</i> parameter, so the <i>pClsidNew</i> parameter is set to <i>clsidOld</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_READREGDB </b></dt>
</dl>
</td>
<td width="60%">
There was an error reading the registry.

</td>
</tr>
</table>
 




## -remarks



<b>CoGetTreatAsClass</b> returns the <a href="https://msdn.microsoft.com/1d7a1677-738a-4258-9afc-e77bd0dcf40f">TreatAs</a> entry in the registry for the specified object. The <b>TreatAs</b> entry, if set, is the CLSID of a registered object (an application) that can emulate the object in question. The <b>TreatAs</b> entry is set through a call to the <a href="https://msdn.microsoft.com/d871879f-ec68-48e1-8ef6-364cf1447d0f">CoTreatAsClass</a> function. Emulation allows an application to open and edit an object of a different format, while retaining the original format of the object. Objects of the original CLSID are activated and treated as objects of the second CLSID. When the object is saved, this may result in loss of edits not supported by the original format. If there is no <b>TreatAs</b> entry for the specified object, this function returns the CLSID of the original object (<i>clsidOld</i>). 





## -see-also




<a href="https://msdn.microsoft.com/d871879f-ec68-48e1-8ef6-364cf1447d0f">CoTreatAsClass</a>
 

 

