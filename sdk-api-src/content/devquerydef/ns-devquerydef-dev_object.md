---
UID: NS:devquerydef._DEV_OBJECT
tech.root: devinst
title: DEV_OBJECT
ms.date: 10/31/2024
targetos: Windows
description: Contains information that represents a device object.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: devquerydef.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DEV_OBJECT, *PDEV_OBJECT
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - devquerydef.h
api_name:
 - _DEV_OBJECT
 - PDEV_OBJECT
 - DEV_OBJECT
f1_keywords:
 - _DEV_OBJECT
 - devquerydef/_DEV_OBJECT
 - PDEV_OBJECT
 - devquerydef/PDEV_OBJECT
 - DEV_OBJECT
 - devquerydef/DEV_OBJECT
dev_langs:
 - c++
helpviewer_keywords:
 - _DEV_OBJECT
---

## -description

Contains information that represents a device object.

## -struct-fields

### -field ObjectType

A value from the [DEV_OBJECT_TYPE](ne-devquerydef-dev_object_type.md) enumeration that specifies the type of this device object.

### -field pszObjectId

The string that is the unique identifier for this particular object among objects of the same type.

### -field cPropertyCount

The count of [DEVPROPERTY](/windows-hardware/drivers/install/devproperty) structures pointed to by *pProperties*.

### -field pProperties

A pointer to an array of 0 or more **DEVPROPERTY** structures.

## -remarks

## -see-also

