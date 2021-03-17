---
UID: NF:mi.MI_Instance_SetElementAt
title: MI_Instance_SetElementAt function (mi.h)
description: Set the value of the element at the given index of an instance.
helpviewer_keywords: ["MI_FLAG_ADOPT","MI_FLAG_BORROW","MI_FLAG_NULL","MI_Instance_SetElementAt","MI_Instance_SetElementAt function [Windows Management Infrastructure (MI)]","mi/MI_Instance_SetElementAt","wmi_v2.mi_instance_setelementat"]
old-location: wmi_v2\mi_instance_setelementat.htm
tech.root: wmi_v2
ms.assetid: 4070af24-b7f9-4484-ab13-d3a52c9e55a0
ms.date: 12/05/2018
ms.keywords: MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NULL, MI_Instance_SetElementAt, MI_Instance_SetElementAt function [Windows Management Infrastructure (MI)], mi/MI_Instance_SetElementAt, wmi_v2.mi_instance_setelementat
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
 - MI_Instance_SetElementAt
 - mi/MI_Instance_SetElementAt
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
 - MI_Instance_SetElementAt
---

# MI_Instance_SetElementAt function


## -description

Set the value of the element at the given index of an instance.

## -parameters

### -param self [in, out]

A pointer to an instance.

### -param index

The position of the element.

### -param value [in, optional]

The new value of the element.

### -param type

The CIM type of the element that will be set.

### -param flags

The bit flags indicates memory management policy and can be any of the following values.



#### MI_FLAG_BORROW

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will not copy the value. The value must stay valid until the instance is deleted.



#### MI_FLAG_ADOPT

Used while adding and setting properties on an <b>MI_Instance</b> to indicate that the instance will adopt the pointer and will be responsible for deleting it.



#### MI_FLAG_NULL

Element value is <b>Null</b>.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

