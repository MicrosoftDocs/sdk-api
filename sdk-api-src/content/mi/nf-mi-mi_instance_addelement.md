---
UID: NF:mi.MI_Instance_AddElement
title: MI_Instance_AddElement function (mi.h)
description: Adds a new property to a dynamic instance (supported only by dynamic instances whose schema may be extended at run time).
helpviewer_keywords: ["MI_FLAG_ADOPT","MI_FLAG_ANY","MI_FLAG_BORROW","MI_FLAG_IN","MI_FLAG_KEY","MI_FLAG_NULL","MI_FLAG_OUT","MI_FLAG_REQUIRED","MI_FLAG_STREAM","MI_Instance_AddElement","MI_Instance_AddElement function [Windows Management Infrastructure (MI)]","mi/MI_Instance_AddElement","wmi_v2.mi_instance_addelement"]
old-location: wmi_v2\mi_instance_addelement.htm
tech.root: wmi_v2
ms.assetid: 51a26894-f391-4281-9e06-2e70fb662aa2
ms.date: 12/05/2018
ms.keywords: MI_FLAG_ADOPT, MI_FLAG_ANY, MI_FLAG_BORROW, MI_FLAG_IN, MI_FLAG_KEY, MI_FLAG_NULL, MI_FLAG_OUT, MI_FLAG_REQUIRED, MI_FLAG_STREAM, MI_Instance_AddElement, MI_Instance_AddElement function [Windows Management Infrastructure (MI)], mi/MI_Instance_AddElement, wmi_v2.mi_instance_addelement
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Instance_AddElement
 - mi/MI_Instance_AddElement
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
 - MI_Instance_AddElement
---

# MI_Instance_AddElement function


## -description

Adds a new property to a dynamic instance (supported only by dynamic instances whose schema may be extended at run time).

## -parameters

### -param self [in, out]

Instance to which the element will be added.

### -param name

A null-terminated string that represents the name of the new element.

### -param value [in, optional]

Element value.

### -param type

Element type.

### -param flags

Flags of the new element that can be a combination of the following flag values.



#### MI_FLAG_KEY (0x00001000)

Element is a key.



#### MI_FLAG_IN (0x00002000)

Parameter is of type In and is passed into a method.



#### MI_FLAG_OUT (0x00004000)

Parameter is of type Out and is returned from a method.



#### MI_FLAG_REQUIRED (0x00008000)

Parameter is required.



#### MI_FLAG_STREAM (0x00100000)

Method parameter will be streamed back to the client from the provider.



#### MI_FLAG_BORROW (0x40000000)

Used while adding and setting properties on an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT (0x80000000)

Used while adding and setting properties on an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> to indicate that the instance will adopt the pointer and will be responsible for deleting it.



#### MI_FLAG_NULL (0x20000000)

Element value is <b>Null</b>.



#### MI_FLAG_ANY (0x0000007F)

Bitmask used to filter out other flags.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_clearelement">MI_Instance_ClearElement</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getelement">MI_Instance_GetElement</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setelement">MI_Instance_SetElement</a>