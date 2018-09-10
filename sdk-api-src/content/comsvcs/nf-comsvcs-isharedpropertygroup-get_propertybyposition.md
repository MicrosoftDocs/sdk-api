---
UID: NF:comsvcs.ISharedPropertyGroup.get_PropertyByPosition
title: ISharedPropertyGroup::get_PropertyByPosition
author: windows-sdk-content
description: Retrieves a reference to an existing shared property with the specified index.
old-location: cos\isharedpropertygroup_get_propertybyposition.htm
tech.root: cossdk
ms.assetid: 186cbf9f-a01b-4331-9f18-645d9e47f106
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISharedPropertyGroup interface [COM+],get_PropertyByPosition method, ISharedPropertyGroup.get_PropertyByPosition, ISharedPropertyGroup::get_PropertyByPosition, _cos_ISharedPropertyGroup_get_PropertyByPosition, comsvcs/ISharedPropertyGroup::get_PropertyByPosition, cos.isharedpropertygroup_get_propertybyposition, get_PropertyByPosition, get_PropertyByPosition method [COM+], get_PropertyByPosition method [COM+],ISharedPropertyGroup interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroup.get_PropertyByPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISharedPropertyGroup::get_PropertyByPosition


## -description


Retrieves a reference to an existing shared property with the specified index.


## -parameters




### -param Index [in]

The numeric index that was used to create the shared property that is retrieved.


### -param ppProperty [out]

A reference to the shared property specified in the <i>Index</i> parameter, or <b>NULL</b> if the property does not exist.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The shared property exists, and a reference to it is returned in the <i>ppProperty</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The shared property with the index specified in the <i>Index</i> parameter does not exist.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a">ISharedProperty</a>



<a href="https://msdn.microsoft.com/e7f23c83-40d3-4b08-a185-cd6e3260e0a9">ISharedPropertyGroup</a>
 

 

