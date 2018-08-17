---
UID: NF:mi.MI_Class_GetMethod
title: MI_Class_GetMethod function
author: windows-sdk-content
description: Gets details of a method based on the method name.
old-location: wmi_v2\mi_class_getmethod.htm
old-project: wmi_v2
ms.assetid: 9e6f6ef0-ca19-4416-baf7-bb2ab1d6d33d
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: MI_Class_GetMethod, MI_Class_GetMethod function [Windows Management Infrastructure (MI)], mi/MI_Class_GetMethod, wmi_v2.mi_class_getmethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Class_GetMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Class_GetMethod function


## -description


Gets details of a method based on the method name.


## -parameters




### -param self [in]

A pointer to the class object from which the method information is to be retrieved.


### -param name [in]

The name of the method to be retrieved.


### -param qualifierSet [out, optional]

A pointer to the variable to receive the returned method qualifier set.   This parameter is optional. The memory associated with the qualifier set is valid until the class object is deleted. When you have finished using the class qualifier set, delete the class object by calling the <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.


### -param parameterSet [out, optional]

A pointer to a variable to receive the returned parameter set. The parameter set also contains the return type and return type qualifier set.   This parameter is optional. The memory associated with the parameter set is valid until the class object is deleted. When you have finished using the parameter set, delete the class object by calling the <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.


### -param index [out, optional]

A pointer to a variable to receive the returned index of the specified method. This parameter is optional.


## -returns



This function returns MI_INLINE MI_Result.



