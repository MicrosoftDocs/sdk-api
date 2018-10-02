---
UID: NE:medparam._MP_Type
title: "_MP_Type"
author: windows-sdk-content
description: The MP_TYPE enumeration specifies the data type for a parameter.
old-location: dshow\mp_type.htm
tech.root: DirectShow
ms.assetid: 9c8851c7-1a72-4dfd-ba2f-e64d8e22f6dc
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: MPT_BOOL, MPT_ENUM, MPT_FLOAT, MPT_INT, MPT_MAX, MP_TYPE, MP_TYPE , MP_TYPE enumeration [DirectShow], MP_TYPEEnumeration, _MP_Type, dshow.mp_type, medparam/MPT_BOOL, medparam/MPT_ENUM, medparam/MPT_FLOAT, medparam/MPT_INT, medparam/MPT_MAX, medparam/MP_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Medparam.h
api_name:
 - MP_TYPE
product: Windows
targetos: Windows
req.typenames: MP_TYPE
req.redist: 
---

# _MP_Type enumeration


## -description



The <code>MP_TYPE</code> enumeration specifies the data type for a parameter.




## -enum-fields




### -field MPT_INT

Value is a signed 32-bit integer.


### -field MPT_FLOAT

Value is a 32-bit IEEE floating-point value.


### -field MPT_BOOL

Value is Boolean. Use the following constants for Boolean parameters:


### -field MPT_ENUM

Value is taken from a set of consecutive integers.


### -field MPT_MAX

Reserved.


## -remarks



To reduce type conversions at run time, all parameters have 32-bit float values, defined as type <b>MP_DATA</b>. The members of this enumeration specify how a given parameter should be interpreted.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/91d2d08b-a55e-492f-a509-9c080cc438df">MP_PARAMINFO</a>
 

 

