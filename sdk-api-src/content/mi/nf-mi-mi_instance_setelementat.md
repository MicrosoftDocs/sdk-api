---
UID: NF:mi.MI_Instance_SetElementAt
title: MI_Instance_SetElementAt function
author: windows-sdk-content
description: Set the value of the element at the given index of an instance.
old-location: wmi_v2\mi_instance_setelementat.htm
old-project: wmi_v2
ms.assetid: 4070af24-b7f9-4484-ab13-d3a52c9e55a0
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NULL, MI_Instance_SetElementAt, MI_Instance_SetElementAt function [Windows Management Infrastructure (MI)], mi/MI_Instance_SetElementAt, wmi_v2.mi_instance_setelementat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Instance_SetElementAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



