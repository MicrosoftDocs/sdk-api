---
UID: NS:mi._MI_ConstUint8AField
title: MI_ConstUint8AField (mi.h)
description: Represents a property inside an MI_Instance structure. (MI_ConstUint8AField)
helpviewer_keywords: ["MI_ConstUint8AField","MI_ConstUint8AField structure [Windows Management Infrastructure (MI)]","MI_FLAG_ADOPT","MI_FLAG_BORROW","MI_FLAG_NOT_MODIFIED","MI_FLAG_NULL","mi/MI_ConstUint8AField","wmi._mi_constuint8afield","wmi_v2.mi_constuint8afield"]
old-location: wmi_v2\mi_constuint8afield.htm
tech.root: wmi_v2
ms.assetid: 532a63c6-c1e6-42aa-94f9-37a9ecb42d35
ms.date: 12/05/2018
ms.keywords: MI_ConstUint8AField, MI_ConstUint8AField structure [Windows Management Infrastructure (MI)], MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, mi/MI_ConstUint8AField, wmi._mi_constuint8afield, wmi_v2.mi_constuint8afield
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
req.typenames: MI_ConstUint8AField
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ConstUint8AField
 - mi/_MI_ConstUint8AField
 - MI_ConstUint8AField
 - mi/MI_ConstUint8AField
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
 - MI_ConstUint8AField
---

# MI_ConstUint8AField structure


## -description

Represents a property inside an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure.

## -struct-fields

### -field value

A field of type <a href="/windows/desktop/api/mi/ns-mi-mi_constuint8a">MI_ConstUint8A</a>.

### -field exists

Indicates whether the field is non-null. Can be set to <b>MI_TRUE</b> or <b>MI_FALSE</b>.

### -field flags

Bit flags indicating memory management policy.



#### MI_FLAG_NOT_MODIFIED ((1 << 25))

Indicates that the property is not modified.



#### MI_FLAG_NULL ((1 << 29))

Element value is <b>Null</b>.



#### MI_FLAG_BORROW ((1 << 30))

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT ((1 << 31))

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will adopt the pointer and will be responsible for deleting it.
