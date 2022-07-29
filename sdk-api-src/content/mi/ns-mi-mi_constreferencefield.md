---
UID: NS:mi._MI_ConstReferenceField
title: MI_ConstReferenceField (mi.h)
description: Represents a property inside an MI_Instance structure. (MI_ConstReferenceField)
helpviewer_keywords: ["MI_ConstReferenceField","MI_ConstReferenceField structure [Windows Management Infrastructure (MI)]","MI_FLAG_ADOPT","MI_FLAG_BORROW","MI_FLAG_NOT_MODIFIED","MI_FLAG_NULL","mi/MI_ConstReferenceField","wmi._mi_constreferencefield","wmi_v2.mi_constreferencefield"]
old-location: wmi_v2\mi_constreferencefield.htm
tech.root: wmi_v2
ms.assetid: 4d93aea8-6d66-4c69-b6f4-22837a692efd
ms.date: 12/05/2018
ms.keywords: MI_ConstReferenceField, MI_ConstReferenceField structure [Windows Management Infrastructure (MI)], MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, mi/MI_ConstReferenceField, wmi._mi_constreferencefield, wmi_v2.mi_constreferencefield
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_ConstReferenceField
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ConstReferenceField
 - mi/_MI_ConstReferenceField
 - MI_ConstReferenceField
 - mi/MI_ConstReferenceField
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_ConstReferenceField
---

# MI_ConstReferenceField structure


## -description

Represents a property inside an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure.

## -struct-fields

### -field value

A pointer to an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure.

### -field exists

Indicates whether the field is non-null. This member can be set to <b>MI_TRUE</b> or <b>MI_FALSE</b>.

### -field flags

Bit flags that indicate the memory management policy.



#### MI_FLAG_NOT_MODIFIED ((1 << 25))

Indicates that the property is not modified.



#### MI_FLAG_NULL ((1 << 29))

The element value is <b>NULL</b>.



#### MI_FLAG_BORROW ((1 << 30))

Used while adding and setting properties on an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT ((1 << 31))

Used while adding and setting properties on an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure to indicate that the instance will adopt the pointer and will be responsible for deleting it.
