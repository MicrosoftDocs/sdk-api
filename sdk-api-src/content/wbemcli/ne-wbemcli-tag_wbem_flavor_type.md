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

# tag_WBEM_FLAVOR_TYPE enumeration


## -description


Lists qualifier flavors.


## -enum-fields




### -field WBEM_FLAVOR_DONT_PROPAGATE

The qualifier is not propagated to instances or derived classes.


### -field WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE

The qualifier is propagated to instances.


### -field WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS

The qualifier is propagated to derived classes. This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.


### -field WBEM_FLAVOR_MASK_PROPAGATION


### -field WBEM_FLAVOR_OVERRIDABLE

When propagated to a derived class or instance, the value of the qualifier can be overridden. Setting EnableOverride is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.


### -field WBEM_FLAVOR_NOT_OVERRIDABLE

The qualifier cannot be overridden in a derived class or instance. Note that being able to override a propagated qualifier is the default.


### -field WBEM_FLAVOR_MASK_PERMISSIONS


### -field WBEM_FLAVOR_ORIGIN_LOCAL

For a class: the property belongs to the derived-most class.

For an instance: the property is modified at the instance level (that is, either a value was supplied or a qualifier was added/modified).


### -field WBEM_FLAVOR_ORIGIN_PROPAGATED

For a class: The property was inherited from the parent class.

For an instance: The property, while inherited from the parent class, has not been modified at the instance level.


### -field WBEM_FLAVOR_ORIGIN_SYSTEM

The property is a standard system property.


### -field WBEM_FLAVOR_MASK_ORIGIN


### -field WBEM_FLAVOR_NOT_AMENDED


### -field WBEM_FLAVOR_AMENDED

The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.


### -field WBEM_FLAVOR_MASK_AMENDED


## -see-also




<a href="https://msdn.microsoft.com/ad602440-dc19-45cf-bf10-a30f514e00bb">IWbemQualifierSet::Put</a>



<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>
 

 

