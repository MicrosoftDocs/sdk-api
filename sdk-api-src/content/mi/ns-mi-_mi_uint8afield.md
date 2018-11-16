---
UID: NS:mi._MI_Uint8AField
title: "_MI_Uint8AField"
author: windows-sdk-content
description: Represents a property inside an MI_Instance structure.
old-location: wmi_v2\mi_uint8afield.htm
tech.root: wmi_v2
ms.assetid: 65fee0fc-c444-4360-b6a0-789f5999f1c5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, MI_Uint8AField, MI_Uint8AField structure [Windows Management Infrastructure (MI)], _MI_Uint8AField, mi/MI_Uint8AField, wmi._mi_uint8afield, wmi_v2.mi_uint8afield
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - MI_Uint8AField
product: Windows
targetos: Windows
req.typenames: MI_Uint8AField
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# _MI_Uint8AField structure


## -description


Represents a property inside an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> structure.


## -struct-fields




### -field value

A field of type <a href="https://msdn.microsoft.com/8d9951eb-7656-4c66-aecb-3e47734a776a">MI_Uint8A</a>.


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

