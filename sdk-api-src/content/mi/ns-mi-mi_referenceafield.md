---
UID: NS:mi._MI_ReferenceAField
title: MI_ReferenceAField (mi.h)
description: Represents a property inside an MI_Instance structure.
helpviewer_keywords: ["MI_FLAG_ADOPT","MI_FLAG_BORROW","MI_FLAG_NOT_MODIFIED","MI_FLAG_NULL","MI_ReferenceAField","MI_ReferenceAField structure [Windows Management Infrastructure (MI)]","mi/MI_ReferenceAField","wmi._mi_referenceafield","wmi_v2.mi_referenceafield"]
old-location: wmi_v2\mi_referenceafield.htm
tech.root: wmi_v2
ms.assetid: 4ccf96f4-4662-4f1d-96d7-650faeff800f
ms.date: 12/05/2018
ms.keywords: MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, MI_ReferenceAField, MI_ReferenceAField structure [Windows Management Infrastructure (MI)], mi/MI_ReferenceAField, wmi._mi_referenceafield, wmi_v2.mi_referenceafield
f1_keywords:
- mi/MI_ReferenceAField
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_ReferenceAField
targetos: Windows
req.typenames: MI_ReferenceAField
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_ReferenceAField structure


## -description


Represents a property inside an <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> structure.


## -struct-fields




### -field value

A field of type <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_referencea">MI_ReferenceA</a>.


### -field exists

Indicates whether the field is non-null. This member can be set to <b>MI_TRUE</b> or <b>MI_FALSE</b>.


### -field flags

Bit flags that indicate the memory management policy.



#### MI_FLAG_NOT_MODIFIED ((1 << 25))

Indicates that the property is not modified.



#### MI_FLAG_NULL ((1 << 29))

The element value is <b>NULL</b>.



#### MI_FLAG_BORROW ((1 << 30))

Used while adding and setting properties on an <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT ((1 << 31))

Used while adding and setting properties on an <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> to indicate that the instance will adopt the pointer and will be responsible for deleting it.

