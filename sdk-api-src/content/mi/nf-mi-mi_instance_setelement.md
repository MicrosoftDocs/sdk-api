---
UID: NF:mi.MI_Instance_SetElement
title: MI_Instance_SetElement function (mi.h)
description: Set the value of the element with the given name in the given instance.
helpviewer_keywords: ["MI_FLAG_ADOPT","MI_FLAG_BORROW","MI_FLAG_NULL","MI_Instance_SetElement","MI_Instance_SetElement function [Windows Management Infrastructure (MI)]","mi/MI_Instance_SetElement","wmi_v2.mi_instance_setelement"]
old-location: wmi_v2\mi_instance_setelement.htm
tech.root: wmi_v2
ms.assetid: 581f8d9f-5421-44ab-a3e2-dfb536a35c2c
ms.date: 12/05/2018
ms.keywords: MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NULL, MI_Instance_SetElement, MI_Instance_SetElement function [Windows Management Infrastructure (MI)], mi/MI_Instance_SetElement, wmi_v2.mi_instance_setelement
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
 - MI_Instance_SetElement
 - mi/MI_Instance_SetElement
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
 - MI_Instance_SetElement
---

# MI_Instance_SetElement function


## -description

Set the value of the element with the given name in the given instance.

## -parameters

### -param self [out]

A pointer to an instance.

### -param name

A null-terminated string that represents the name of the element that will be set.

### -param value [in, optional]

The new value for the element.

### -param type

The CIM type of the element that will be set.

### -param flags

Bit flags indicating memory management policy.



#### MI_FLAG_BORROW

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will adopt the pointer and will be responsible for deleting it.



#### MI_FLAG_NULL

Element value is <b>Null</b>.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

By default, all memory referred to by the value parameter is copied. By passing the flag MI_FLAG_BORROW, memory pointers within the value structure are stored directly in the instance's element. The caller must guarantee that the memory outlives the instance.

