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

# IWbemQualifierSet::Put


## -description


The <b>IWbemQualifierSet::Put</b> method writes the named qualifier and value. The new qualifier overwrites the previous  value of the same name. If the qualifier does not exist, it is created.

Sometimes it is not possible to write the value of a qualifier, for example, if the qualifier is  propagated from another object. Typically, propagated qualifiers are read-only, but they can be overridden. For more information, see 
<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>.

When using the <a href="https://msdn.microsoft.com/library/windows/hardware/dn895751">Key</a> qualifier, it is not necessary to specify any flavors or propagation rules.

The user may not create qualifiers with names that begin or end with an underscore (_). This is reserved for system classes and properties.


## -parameters




### -param wszName [in]

Name of the qualifier that is being written. The pointer is treated as read-only.


### -param pVal [in]

Cannot be <b>NULL</b>. This must point to a valid <b>VARIANT</b> that contains the qualifier value to be written. The pointer is treated as read-only. It is the caller's responsibility to call <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a> on this pointer after the value is not required.

Only variants and arrays of type <b>VT_I4</b>, <b>VT_R8</b>, <b>VT_BSTR</b>, <b>VT_BOOL</b> are supported.


### -param lFlavor [in]

Desired qualifier flavors for this qualifier.  The following list lists the appropriate constants for <i>lFlavor</i>. The default value is zero (0).



#### WBEM_FLAVOR_OVERRIDABLE (0 (0x0))

The qualifier value can be overridden in a derived class or an instance. This is the default. Using this constant is the same as using the <b>EnableOverride</b> flag.



#### WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE (1 (0x1))

The qualifier is propagated to instances. Using this constant is the same as using the <b>ToInstance</b> flag.



#### WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS (2 (0x2))

The qualifier is propagated to derived classes. Using this constant is the same as using the <b>ToSubClass</b> flag.



#### WBEM_FLAVOR_NOT_OVERRIDABLE (16 (0x10))

The qualifier value cannot be overridden in a derived class or an instance. Using this constant is the same as using the <b>DisableOverride</b> flag.



#### WBEM_FLAVOR_AMENDED (128 (0x80))

The qualifier is localized. Using this constant is the same as using the <b>Amended</b> flag.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>
 

 

