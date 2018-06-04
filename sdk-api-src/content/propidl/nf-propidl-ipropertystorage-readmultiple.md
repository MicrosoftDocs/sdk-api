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

# IPropertyStorage::ReadMultiple


## -description


The
		<b>ReadMultiple</b> method
			 reads specified properties from the current property set.


## -parameters




### -param cpspec [in]

The numeric count of properties to be specified in the <i>rgpspec</i> array. The value of this parameter can  be set to zero; however, that defeats the purpose of the method as no properties are thereby read, regardless of the values set in <i>rgpspec</i>.


### -param rgpspec [in]

An array of 
<a href="https://msdn.microsoft.com/5bb3b9c6-ab82-498c-94f9-13a9ffa7452b">PROPSPEC</a> structures specifies which properties are  read. Properties can be specified either by a property ID or by an optional string name. It is not necessary to specify properties in any particular order in the array. The array can contain duplicate properties, resulting in duplicate property values on return for simple properties. Nonsimple properties should return access denied on an attempt to open them a second time. The array can contain a mixture of property IDs and string IDs.


### -param rgpropvar [out]

Caller-allocated array of a 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that, on return, contains the values of the properties specified by the corresponding elements in the <i>rgpspec</i> array. The array must be at least large enough to hold values of the <i>cpspec</i> parameter of the 
<b>PROPVARIANT</b> structure. The <i>cpspec</i> parameter specifies the number of properties set in the array. The caller is not required to initialize these 
<b>PROPVARIANT</b> structure values in any specific  order. However, the implementation must fill all members correctly on return. If there is no other appropriate value, the implementation must set the <b>vt</b> member of each 
<b>PROPVARIANT</b> structure to <b>VT_EMPTY</b>.


## -returns




						This method supports the standard return value <b>E_UNEXPECTED</b>, as well as the following:

This function can also return any file system errors or Win32 errors wrapped in an <b>HRESULT</b> data type. For more information, see 
<a href="_com_error_handling_strategies">Error Handling Strategies</a>.

For more information, see 
<a href="https://msdn.microsoft.com/7540966f-a3b2-46c9-9e04-b15133a517eb">Property Storage Considerations</a>.




## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IPropertyStorage::WriteMultiple</a>



<a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">IPropertyStorage::WritePropertyNames</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>



<a href="https://msdn.microsoft.com/f0d0664a-2cfd-4eb0-b1d5-47d1545394fd">StgCreatePropSetStg Sample</a>



<a href="https://msdn.microsoft.com/c5807dd9-2928-497b-9446-729dcaeebc8a">WriteRead Sample</a>
 

 

