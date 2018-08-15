---
UID: NF:mi.MI_Class_GetParentClassName
title: MI_Class_GetParentClassName function
author: windows-sdk-content
description: Gets the parent class name of the specified class.
old-location: wmi_v2\mi_class_getparentclassname.htm
old-project: wmi_v2
ms.assetid: a7e183f1-1136-46e0-a53d-39d06767e380
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Class_GetParentClassName, MI_Class_GetParentClassName function [Windows Management Infrastructure (MI)], mi/MI_Class_GetParentClassName, wmi_v2.mi_class_getparentclassname
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
 - MI_Class_GetParentClassName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Class_GetParentClassName function


## -description


Gets the parent class name of the specified class.


## -parameters




### -param self [in]

A pointer to the class from which to retrieve the parent class name.


### -param name

A pointer to a pointer to the returned parent class name value. This string is owned by the class and does not need to be deleted. If there is no parent class, this will be <b>NULL</b>.


## -returns



This function returns MI_INLINE MI_Result.



