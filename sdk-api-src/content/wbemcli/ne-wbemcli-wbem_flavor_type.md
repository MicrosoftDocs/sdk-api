---
UID: NE:wbemcli.tag_WBEM_FLAVOR_TYPE
title: WBEM_FLAVOR_TYPE (wbemcli.h)
description: Lists qualifier flavors.
helpviewer_keywords: ["WBEM_FLAVOR_AMENDED","WBEM_FLAVOR_DONT_PROPAGATE","WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS","WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE","WBEM_FLAVOR_MASK_AMENDED","WBEM_FLAVOR_MASK_ORIGIN","WBEM_FLAVOR_MASK_PERMISSIONS","WBEM_FLAVOR_MASK_PROPAGATION","WBEM_FLAVOR_NOT_AMENDED","WBEM_FLAVOR_NOT_OVERRIDABLE","WBEM_FLAVOR_ORIGIN_LOCAL","WBEM_FLAVOR_ORIGIN_PROPAGATED","WBEM_FLAVOR_ORIGIN_SYSTEM","WBEM_FLAVOR_OVERRIDABLE","WBEM_FLAVOR_TYPE","WBEM_FLAVOR_TYPE enumeration [Windows Management Instrumentation]","wbemcli/WBEM_FLAVOR_AMENDED","wbemcli/WBEM_FLAVOR_DONT_PROPAGATE","wbemcli/WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS","wbemcli/WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE","wbemcli/WBEM_FLAVOR_MASK_AMENDED","wbemcli/WBEM_FLAVOR_MASK_ORIGIN","wbemcli/WBEM_FLAVOR_MASK_PERMISSIONS","wbemcli/WBEM_FLAVOR_MASK_PROPAGATION","wbemcli/WBEM_FLAVOR_NOT_AMENDED","wbemcli/WBEM_FLAVOR_NOT_OVERRIDABLE","wbemcli/WBEM_FLAVOR_ORIGIN_LOCAL","wbemcli/WBEM_FLAVOR_ORIGIN_PROPAGATED","wbemcli/WBEM_FLAVOR_ORIGIN_SYSTEM","wbemcli/WBEM_FLAVOR_OVERRIDABLE","wbemcli/WBEM_FLAVOR_TYPE","wmi.wbem_flavor_type"]
old-location: wmi\wbem_flavor_type.htm
tech.root: wmi
ms.assetid: A21ED0FD-1207-42B6-92AE-6080D0E98771
ms.date: 12/05/2018
ms.keywords: WBEM_FLAVOR_AMENDED, WBEM_FLAVOR_DONT_PROPAGATE, WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS, WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE, WBEM_FLAVOR_MASK_AMENDED, WBEM_FLAVOR_MASK_ORIGIN, WBEM_FLAVOR_MASK_PERMISSIONS, WBEM_FLAVOR_MASK_PROPAGATION, WBEM_FLAVOR_NOT_AMENDED, WBEM_FLAVOR_NOT_OVERRIDABLE, WBEM_FLAVOR_ORIGIN_LOCAL, WBEM_FLAVOR_ORIGIN_PROPAGATED, WBEM_FLAVOR_ORIGIN_SYSTEM, WBEM_FLAVOR_OVERRIDABLE, WBEM_FLAVOR_TYPE, WBEM_FLAVOR_TYPE enumeration [Windows Management Instrumentation], wbemcli/WBEM_FLAVOR_AMENDED, wbemcli/WBEM_FLAVOR_DONT_PROPAGATE, wbemcli/WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS, wbemcli/WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE, wbemcli/WBEM_FLAVOR_MASK_AMENDED, wbemcli/WBEM_FLAVOR_MASK_ORIGIN, wbemcli/WBEM_FLAVOR_MASK_PERMISSIONS, wbemcli/WBEM_FLAVOR_MASK_PROPAGATION, wbemcli/WBEM_FLAVOR_NOT_AMENDED, wbemcli/WBEM_FLAVOR_NOT_OVERRIDABLE, wbemcli/WBEM_FLAVOR_ORIGIN_LOCAL, wbemcli/WBEM_FLAVOR_ORIGIN_PROPAGATED, wbemcli/WBEM_FLAVOR_ORIGIN_SYSTEM, wbemcli/WBEM_FLAVOR_OVERRIDABLE, wbemcli/WBEM_FLAVOR_TYPE, wmi.wbem_flavor_type
f1_keywords:
- wbemcli/WBEM_FLAVOR_TYPE
dev_langs:
- c++
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
- HeaderDef
api_location:
- Wbemcli.h
api_name:
- WBEM_FLAVOR_TYPE
targetos: Windows
req.typenames: WBEM_FLAVOR_TYPE
req.redist: 
ms.custom: 19H1
---

# WBEM_FLAVOR_TYPE enumeration


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




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-put">IWbemQualifierSet::Put</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>
 

 

