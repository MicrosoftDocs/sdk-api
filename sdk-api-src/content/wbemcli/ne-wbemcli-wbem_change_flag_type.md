---
UID: NE:wbemcli.tag_WBEM_CHANGE_FLAG_TYPE
title: WBEM_CHANGE_FLAG_TYPE (wbemcli.h)
description: Contains method parameter flags.
helpviewer_keywords: ["WBEM_CHANGE_FLAG_TYPE","WBEM_CHANGE_FLAG_TYPE enumeration [Windows Management Instrumentation]","WBEM_FLAG_ADVISORY","WBEM_FLAG_CREATE_ONLY","WBEM_FLAG_CREATE_OR_UPDATE","WBEM_FLAG_UPDATE_COMPATIBLE","WBEM_FLAG_UPDATE_FORCE_MODE","WBEM_FLAG_UPDATE_ONLY","WBEM_FLAG_UPDATE_SAFE_MODE","WBEM_MASK_UPDATE_MODE","wbemcli/WBEM_CHANGE_FLAG_TYPE","wbemcli/WBEM_FLAG_ADVISORY","wbemcli/WBEM_FLAG_CREATE_ONLY","wbemcli/WBEM_FLAG_CREATE_OR_UPDATE","wbemcli/WBEM_FLAG_UPDATE_COMPATIBLE","wbemcli/WBEM_FLAG_UPDATE_FORCE_MODE","wbemcli/WBEM_FLAG_UPDATE_ONLY","wbemcli/WBEM_FLAG_UPDATE_SAFE_MODE","wbemcli/WBEM_MASK_UPDATE_MODE","wmi.wbem_change_flag_type"]
old-location: wmi\wbem_change_flag_type.htm
tech.root: wmi
ms.assetid: B36B7D62-13C9-401F-A6C0-7C498A139AEC
ms.date: 12/05/2018
ms.keywords: WBEM_CHANGE_FLAG_TYPE, WBEM_CHANGE_FLAG_TYPE enumeration [Windows Management Instrumentation], WBEM_FLAG_ADVISORY, WBEM_FLAG_CREATE_ONLY, WBEM_FLAG_CREATE_OR_UPDATE, WBEM_FLAG_UPDATE_COMPATIBLE, WBEM_FLAG_UPDATE_FORCE_MODE, WBEM_FLAG_UPDATE_ONLY, WBEM_FLAG_UPDATE_SAFE_MODE, WBEM_MASK_UPDATE_MODE, wbemcli/WBEM_CHANGE_FLAG_TYPE, wbemcli/WBEM_FLAG_ADVISORY, wbemcli/WBEM_FLAG_CREATE_ONLY, wbemcli/WBEM_FLAG_CREATE_OR_UPDATE, wbemcli/WBEM_FLAG_UPDATE_COMPATIBLE, wbemcli/WBEM_FLAG_UPDATE_FORCE_MODE, wbemcli/WBEM_FLAG_UPDATE_ONLY, wbemcli/WBEM_FLAG_UPDATE_SAFE_MODE, wbemcli/WBEM_MASK_UPDATE_MODE, wmi.wbem_change_flag_type
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
targetos: Windows
req.typenames: WBEM_CHANGE_FLAG_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_CHANGE_FLAG_TYPE
 - wbemcli/tag_WBEM_CHANGE_FLAG_TYPE
 - WBEM_CHANGE_FLAG_TYPE
 - wbemcli/WBEM_CHANGE_FLAG_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_CHANGE_FLAG_TYPE
---

# WBEM_CHANGE_FLAG_TYPE enumeration


## -description

Contains method parameter flags.

## -enum-fields

### -field WBEM_FLAG_CREATE_OR_UPDATE:0

The class is created if it does not exist, or overwritten if it exists already.

### -field WBEM_FLAG_UPDATE_ONLY:0x1

The class is overwritten if it exists already, but will not be created if it does not exist.The class must exist for the call to be successful.

### -field WBEM_FLAG_CREATE_ONLY:0x2

This flag is used for creation only. The call fails if the class already exists.

### -field WBEM_FLAG_UPDATE_COMPATIBLE:0

This flag allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is just to nonimportant qualifiers (for example, the <b>Description</b> qualifier). This is the default behavior for this call and is used for compatibility with previous versions of Windows Management. If the class has instances or changes are to important qualifiers, the update fails.

### -field WBEM_FLAG_UPDATE_SAFE_MODE:0x20

This flag allows updates of classes even if there are child classes as long as the change does not cause any conflicts with child classes. An example of an update this flag would allow would be to add a new property to the base class that was not previously mentioned in any of the child classes. If the class has instances, the update fails.

### -field WBEM_FLAG_UPDATE_FORCE_MODE:0x40

This flag forces updates of classes when conflicting child classes exist. An example of an update this flag would force would be if a class qualifier were defined in a child class, and the base class tried to add the same qualifier which conflicted with the existing one. In force mode, this conflict would be resolved by deleting the conflicting qualifier in the child class.

### -field WBEM_MASK_UPDATE_MODE:0x60

A mask value that can be used to simplify testing for the other flag values.

### -field WBEM_FLAG_ADVISORY:0x10000

Reserved for future use.

