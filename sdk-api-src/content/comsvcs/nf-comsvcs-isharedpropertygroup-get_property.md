---
UID: NF:comsvcs.ISharedPropertyGroup.get_Property
title: ISharedPropertyGroup::get_Property method
author: windows-driver-content
description: Retrieves a reference to an existing shared property with the specified name.
old-location: cos\isharedpropertygroup_get_property.htm
old-project: cossdk
ms.assetid: ffbd82a8-35d5-4c9b-bf03-91f48dddc189
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ISharedPropertyGroup, ISharedPropertyGroup interface [COM+], get_Property method, ISharedPropertyGroup::get_Property, _cos_ISharedPropertyGroup_get_Property, comsvcs/ISharedPropertyGroup::get_Property, cos.isharedpropertygroup_get_property, get_Property method [COM+], get_Property method [COM+], ISharedPropertyGroup interface, get_Property,ISharedPropertyGroup.get_Property
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ISharedPropertyGroup.get_Property
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISharedPropertyGroup::get_Property method


## -description


Retrieves a reference to an existing shared property with the specified name.


## -parameters




### -param Name [in]

The name that was used to create the shared property that is retrieved.


### -param ppProperty [out]

A reference to the shared property specified in the <i>Name</i> parameter, or <b>NULL</b> if the property does not exist.


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
The shared property with the name specified in the <i>Name</i> parameter does not exist.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a">ISharedProperty</a>



<a href="https://msdn.microsoft.com/e7f23c83-40d3-4b08-a185-cd6e3260e0a9">ISharedPropertyGroup</a>
 

 

