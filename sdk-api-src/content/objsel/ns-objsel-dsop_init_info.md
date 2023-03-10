---
UID: NS:objsel._DSOP_INIT_INFO
title: DSOP_INIT_INFO (objsel.h)
description: The DSOP_INIT_INFO structure contains data required to initialize an object picker dialog box. This structure is used with the IDsObjectPicker::Initialize method.
helpviewer_keywords: ["*PDSOP_INIT_INFO","DSOP_FLAG_MULTISELECT","DSOP_FLAG_SKIP_TARGET_COMPUTER_DC_CHECK","DSOP_INIT_INFO","DSOP_INIT_INFO structure [Active Directory]","PDSOP_INIT_INFO","PDSOP_INIT_INFO structure pointer [Active Directory]","_glines_dsop_init_info","ad.dsop__init__info","ad.dsop_init_info","objsel/DSOP_INIT_INFO","objsel/PDSOP_INIT_INFO"]
old-location: ad\dsop_init_info.htm
tech.root: ad
ms.assetid: 6d070185-e0b6-4c24-9941-95bca2f33192
ms.date: 12/05/2018
ms.keywords: '*PDSOP_INIT_INFO, DSOP_FLAG_MULTISELECT, DSOP_FLAG_SKIP_TARGET_COMPUTER_DC_CHECK, DSOP_INIT_INFO, DSOP_INIT_INFO structure [Active Directory], PDSOP_INIT_INFO, PDSOP_INIT_INFO structure pointer [Active Directory], _glines_dsop_init_info, ad.dsop__init__info, ad.dsop_init_info, objsel/DSOP_INIT_INFO, objsel/PDSOP_INIT_INFO'
req.header: objsel.h
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
targetos: Windows
req.typenames: DSOP_INIT_INFO, *PDSOP_INIT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSOP_INIT_INFO
 - objsel/_DSOP_INIT_INFO
 - PDSOP_INIT_INFO
 - objsel/PDSOP_INIT_INFO
 - DSOP_INIT_INFO
 - objsel/DSOP_INIT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objsel.h
api_name:
 - DSOP_INIT_INFO
---

# DSOP_INIT_INFO structure


## -description

The <b>DSOP_INIT_INFO</b> structure contains data required to initialize an object picker dialog box. This structure is used with the 
<a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-initialize">IDsObjectPicker::Initialize</a> method.

## -struct-fields

### -field cbSize

Contains the size, in bytes, of the structure.

### -field pwzTargetComputer

Pointer to a null-terminated Unicode string that contains the name of the target computer. The dialog box operates as if it is running on the target computer, using the target computer to determine the joined domain and enterprise. If this value is <b>NULL</b>, the target computer is the local computer.

### -field cDsScopeInfos

Specifies the number of elements in the <b>aDsScopeInfos</b> array.

### -field aDsScopeInfos

Pointer to an array of 
<a href="/windows/desktop/api/objsel/ns-objsel-dsop_scope_init_info">DSOP_SCOPE_INIT_INFO</a> structures that describe the scopes from which the user can select objects. This member cannot be <b>NULL</b> and the array must contain at least one element because the object picker cannot operate without at least one scope.

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

<a href="/windows/desktop/api/objsel/ns-objsel-dsop_scope_init_info">DSOP_SCOPE_INIT_INFO</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>



<a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-initialize">IDsObjectPicker::Initialize</a>