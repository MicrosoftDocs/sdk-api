---
UID: NF:mi.MI_Class_GetNameSpace
title: MI_Class_GetNameSpace function
author: windows-sdk-content
description: Gets the namespace name of the specified class.
old-location: wmi_v2\mi_class_getnamespace.htm
old-project: wmi_v2
ms.assetid: 64ee42d6-d6ad-4a41-83f4-48de191a853c
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_Class_GetNameSpace, MI_Class_GetNameSpace function [Windows Management Infrastructure (MI)], mi/MI_Class_GetNameSpace, wmi_v2.mi_class_getnamespace
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
tech.root: 
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Class_GetNameSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Class_GetNameSpace function


## -description


Gets the namespace name of the specified class.


## -parameters




### -param self [in]

A pointer to the class from which to get the namespace name.


### -param nameSpace

A pointer to a pointer to the returned namespace name value. This string is owned by the class and does not need to be deleted.


## -returns



This function returns MI_INLINE MI_Result.



