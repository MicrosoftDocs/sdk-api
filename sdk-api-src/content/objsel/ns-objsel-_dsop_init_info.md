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

# _DSOP_INIT_INFO structure


## -description


The <b>DSOP_INIT_INFO</b> structure contains data required to initialize an object picker dialog box. This structure is used with the 
<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a> method.


## -struct-fields




### -field cbSize

Contains the size, in bytes, of the structure.


### -field pwzTargetComputer

Pointer to a null-terminated Unicode string that contains the name of the target computer. The dialog box operates as if it is running on the target computer, using the target computer to determine the joined domain and enterprise. If this value is <b>NULL</b>, the target computer is the local computer.


### -field cDsScopeInfos

Specifies the number of elements in the <b>aDsScopeInfos</b> array.


### -field aDsScopeInfos

Pointer to an array of 
<a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a> structures that describe the scopes from which the user can select objects. This member cannot be <b>NULL</b> and the array must contain at least one element because the object picker cannot operate without at least one scope.


### -field flOptions

Flags that determine the object picker options. This member can be zero or a combination of one or more of the following flags.



#### DSOP_FLAG_MULTISELECT (0x00000001)

If this flag is set, the user can select multiple objects. If this flag is not set, the user can select only one object.



#### DSOP_FLAG_SKIP_TARGET_COMPUTER_DC_CHECK (0x00000002)

If this flag is set and the <b>DSOP_SCOPE_TYPE_TARGET_COMPUTER</b> flag is set in the <b>aDsScopeInfos</b> array, the target computer is always included in the <b>Look in</b> drop-down list.

If this flag is not set and the target computer is an up-level or down-level domain controller, the <b>DSOP_SCOPE_TYPE_TARGET_COMPUTER</b> flag is ignored and the target computer is not included in the <b>Look in</b> drop-down list.

To save time during initialization, this flag should be set if it is known that the target computer is not a domain controller. However, if the target computer is a domain controller, this flag should not be set because it is better for the user to select domain objects from the domain scope rather than from the domain controller itself.


### -field cAttributesToFetch

Contains the number of elements in the <b>apwzAttributeNames</b> array. This member can be zero.


### -field apwzAttributeNames

Pointer to an array of null-terminated Unicode strings that contain the names of the attributes to retrieve for each selected object. If <b>cAttributesToFetch</b> is zero, this member is ignored.


## -see-also




<a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>
 

 

