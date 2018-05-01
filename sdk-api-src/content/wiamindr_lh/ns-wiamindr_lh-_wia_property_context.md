---
UID: NS:wiamindr_lh._WIA_PROPERTY_CONTEXT
title: "_WIA_PROPERTY_CONTEXT"
author: windows-driver-content
description: The WIA_PROPERTY_CONTEXT structure stores property identifiers and their context.
old-location: image\wia_property_context.htm
old-project: image
ms.assetid: afe92cb5-519a-46a3-a66d-c01b6a2c780b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWIA_PROPERTY_CONTEXT, PWIA_PROPERTY_CONTEXT, PWIA_PROPERTY_CONTEXT structure pointer [Imaging Devices], WIA_PROPERTY_CONTEXT, WIA_PROPERTY_CONTEXT structure [Imaging Devices], _WIA_PROPERTY_CONTEXT, image.wia_property_context, wiamindr_lh/PWIA_PROPERTY_CONTEXT, wiamindr_lh/WIA_PROPERTY_CONTEXT, wiastrct_044e9a49-3276-42f5-a903-d21969cf6168.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: WIA_PROPERTY_CONTEXT, *PWIA_PROPERTY_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamindr_lh.h
api_name:
-	WIA_PROPERTY_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WIA_PROPERTY_CONTEXT structure


## -description


The WIA_PROPERTY_CONTEXT structure stores property identifiers and their context. 


## -struct-fields




### -field cProps

Specifies the number of property identifiers stored in this structure.


### -field pProps

Is an array of property identifiers that indicate the properties being written.


### -field pChanged

Is an array of Boolean values indicating which properties are changing. A member of this array is <b>TRUE</b> if the corresponding property is changing, and <b>FALSE</b> if the corresponding property is not changing. That is, if <b>pChanged</b>[n] is <b>TRUE</b>, <b>pProps</b>[n] will be changed, and if <b>pChanged</b>[n] is <b>FALSE</b>, <b>pProps</b>[n] will not be changed.


## -remarks



The Boolean values indicate whether the corresponding property is being written (changed) by an application calling <b>IPropertyStorage::WriteMultiple</b>, which is described in the Microsoft Windows SDK documentation.

Several WIA service library functions use the WIA_PROPERTY_CONTEXT structure. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff549167">wiasCreatePropContext</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff549195">wiasFreePropContext</a> functions use it when a property context is created or freed. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff549271">wiasIsPropChanged</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff549374">wiasSetPropChanged</a> use this structure to determine whether a property changed, and to modify a property context when the property does change. The <b>wiasGetChangedValue</b><i>Xxx</i> functions use this structure to determine whether a property of a certain type has changed. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff549448">wiasUpdateValidFormat</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff549441">wiasUpdateScanRect</a> use it to, respectively, update a property context and to update the scanning area sizes for a scanning device.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549167">wiasCreatePropContext</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549195">wiasFreePropContext</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549200">wiasGetChangedValueFloat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549211">wiasGetChangedValueGuid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549214">wiasGetChangedValueLong</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549219">wiasGetChangedValueStr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549271">wiasIsPropChanged</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549374">wiasSetPropChanged</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549441">wiasUpdateScanRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549448">wiasUpdateValidFormat</a>
 

 

