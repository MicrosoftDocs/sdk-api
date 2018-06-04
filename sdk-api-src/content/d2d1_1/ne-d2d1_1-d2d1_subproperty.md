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

# D2D1_SUBPROPERTY enumeration


## -description


Specifies the indices of the system sub-properties that may be present in any property.


## -enum-fields




### -field D2D1_SUBPROPERTY_DISPLAYNAME

The name for the parent property.


### -field D2D1_SUBPROPERTY_ISREADONLY

A Boolean indicating whether the parent property is writeable.


### -field D2D1_SUBPROPERTY_MIN

The minimum value that can be set to the parent property.


### -field D2D1_SUBPROPERTY_MAX

The maximum value that can be set to the parent property.


### -field D2D1_SUBPROPERTY_DEFAULT

The default value of the parent property.


### -field D2D1_SUBPROPERTY_FIELDS

An array of name/index pairs that indicate the possible values that can be set to the parent property.


### -field D2D1_SUBPROPERTY_INDEX

An index sub-property used by the elements of the <b>D2D1_SUBPROPERTY_FIELDS</b> array.


### -field D2D1_SUBPROPERTY_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>



<a href="https://msdn.microsoft.com/36873134-cb0e-4ba2-bddb-95b2cc92afff">ID2D1Properties::GetPropertyName</a>



<a href="https://msdn.microsoft.com/9c4b86d1-db5b-41cd-9dd4-85a8bb03dd20">ID2D1Properties::GetPropertyNameLength</a>



<a href="https://msdn.microsoft.com/6ba7ba8e-63fd-44a1-9a03-565b2e2a128c">ID2D1Properties::GetSubProperties</a>



<a href="https://msdn.microsoft.com/42e80588-9e80-4f30-9a3c-77b64f88ff7a">ID2D1Properties::GetType</a>



<a href="https://msdn.microsoft.com/01678e13-df23-47bb-9af7-9f2ecaf03577">ID2D1Properties::GetValue</a>



<a href="https://msdn.microsoft.com/fd65a610-9552-4efe-9050-715cb672acc8">ID2D1Properties::GetValueSize</a>



<a href="https://msdn.microsoft.com/7b21bcc0-b76e-4802-a8c4-ffba5ac8fa19">ID2D1Properties::SetValue</a>
 

 

