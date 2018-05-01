---
UID: NF:wiautil.CWiauPropertyList.DefineProperty
title: CWiauPropertyList::DefineProperty method
author: windows-driver-content
description: The CWiauPropertyList::DefineProperty method adds a property definition to a property list object.
old-location: image\cwiaupropertylist_defineproperty.htm
old-project: image
ms.assetid: 599c97af-1285-4fb9-af0b-edcd48249692
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiauPropertyList, CWiauPropertyList interface [Imaging Devices], DefineProperty method, CWiauPropertyList::DefineProperty, DefineProperty method [Imaging Devices], DefineProperty method [Imaging Devices], CWiauPropertyList interface, DefineProperty,CWiauPropertyList.DefineProperty, image.cwiaupropertylist_defineproperty, wiauFncs_8be9dc72-0d8c-4894-aab0-47a312d9fae7.xml, wiautil/CWiauPropertyList::DefineProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiautil.h
req.include-header: Wiautil.h, Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiautil.h
api_name:
-	CWiauPropertyList.DefineProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiauPropertyList::DefineProperty method


## -description


The <b>CWiauPropertyList::DefineProperty</b> method adds a property definition to a property list object.


## -parameters




### -param pIdx

Pointer to a memory location that receives the index for the newly added property. Many other methods in this class use a property's index in order to identify the property.


### -param PropId

Specifies a property ID constant.


### -param PropName

Pointer to a name string for the property.


### -param Access

Specifies the type of access for the property, usually either WIA_PROP_READ (read-only) or WIA_PROP_RW (read/write).


### -param SubType

Specifies the property subtype, one of WIA_PROP_FLAG, WIA_PROP_LIST, WIA_PROP_RANGE, or WIA_PROP_NONE. The first three constants indicate, respectively, that a property is a set of flag values, a list of values, or a range of values. The fourth constant indicates that a property is none of these.


## -returns



This method returns S_OK if it is able to define a property successfully. If the property list does not have enough room for an additional property, the method returns E_FAIL.




## -remarks



The WIA_PROP_<i>XXX</i> constants are defined in the Microsoft Windows SDK documentation.

Before a property can be added to a property list, the property list must be initialized. Do this by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540396">CWiauPropertyList::Init</a> method.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540396">CWiauPropertyList::Init</a>
 

 

