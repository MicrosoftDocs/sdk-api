---
UID: NS:mi._MI_ConstSint64Field
title: MI_ConstSint64Field (mi.h)
description: Represents a property inside an MI_Instance structure. (MI_ConstSint64Field)
helpviewer_keywords: ["MI_ConstSint64Field","MI_ConstSint64Field structure [Windows Management Infrastructure (MI)]","MI_FLAG_ADOPT","MI_FLAG_BORROW","MI_FLAG_NOT_MODIFIED","MI_FLAG_NULL","mi/MI_ConstSint64Field","wmi._mi_constsint64field","wmi_v2.mi_constsint64field"]
old-location: wmi_v2\mi_constsint64field.htm
tech.root: wmi_v2
ms.assetid: fff4b692-dbd8-4b4d-b62f-9af629c9862e
ms.date: 12/05/2018
ms.keywords: MI_ConstSint64Field, MI_ConstSint64Field structure [Windows Management Infrastructure (MI)], MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, mi/MI_ConstSint64Field, wmi._mi_constsint64field, wmi_v2.mi_constsint64field
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
req.typenames: MI_ConstSint64Field
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ConstSint64Field
 - mi/_MI_ConstSint64Field
 - MI_ConstSint64Field
 - mi/MI_ConstSint64Field
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
 - MI_ConstSint64Field
---

# MI_ConstSint64Field structure


## -description

Represents a property inside an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure.

## -struct-fields

### -field value

A field of type <b>MI_Sint64</b>.

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
