---
UID: NF:mi.MI_Class_GetClassQualifierSet
title: MI_Class_GetClassQualifierSet function
author: windows-driver-content
description: Gets the qualifier set that is associated with the specified class object.
old-location: wmi_v2\mi_class_getclassqualifierset.htm
old-project: wmi_v2
ms.assetid: 900ae879-a728-43a9-8dcb-de20a50f8dce
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Class_GetClassQualifierSet, MI_Class_GetClassQualifierSet function [Windows Management Infrastructure (MI)], mi/MI_Class_GetClassQualifierSet, wmi_v2.mi_class_getclassqualifierset
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	MI_Class_GetClassQualifierSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Class_GetClassQualifierSet function


## -description


Gets the qualifier set that is associated with the specified class object.


## -parameters




### -param self [in]

A pointer to the class from which to get the qualifier set.


### -param qualifierSet [out, optional]

A pointer to the variable to receive the returned class qualifier set.  This parameter is optional. The memory associated with the qualifier set is valid until the class object is deleted. When you have finished using the class qualifier set, delete the class object by calling the <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function.


## -returns



This function returns MI_INLINE MI_Result.



