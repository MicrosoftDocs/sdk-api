---
UID: NS:mi._MI_DatetimeField
title: "_MI_DatetimeField"
author: windows-sdk-content
description: Represents a property inside an MI_Instance structure.
old-location: wmi_v2\mi_datetimefield.htm
old-project: wmi_v2
ms.assetid: aea7c78a-de7a-48ff-950f-836c1b6c5176
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_DatetimeField, MI_DatetimeField structure [Windows Management Infrastructure (MI)], MI_FLAG_ADOPT, MI_FLAG_BORROW, MI_FLAG_NOT_MODIFIED, MI_FLAG_NULL, _MI_DatetimeField, mi/MI_DatetimeField, wmi._mi_datetimefield, wmi_v2.mi_datetimefield
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_DatetimeField
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DatetimeField
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_DatetimeField structure


## -description


Represents a property inside an <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> structure.


## -struct-fields




### -field value

A field of type <a href="https://msdn.microsoft.com/2f7d857f-5115-40a2-84d9-a4429d935de1">MI_Datetime</a>.


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

