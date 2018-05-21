---
UID: NF:mi.MI_Class_Clone
title: MI_Class_Clone function
author: windows-driver-content
description: Clones an MI_Class object.
old-location: wmi_v2\mi_class_clone.htm
old-project: wmi_v2
ms.assetid: a95b867c-7567-4ea4-a02c-049002de2109
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_Class_Clone, MI_Class_Clone function [Windows Management Infrastructure (MI)], mi/MI_Class_Clone, wmi_v2.mi_class_clone
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
-	MI_Class_Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Class_Clone function


## -description


Clones an <a href="https://msdn.microsoft.com/7f02e0fa-9e58-455d-9cf4-1d1244c44422">MI_Class</a> object.


## -parameters




### -param self [in]

A pointer to the class to be cloned.


### -param newClass

A pointer to a pointer to the newly created class. When you have finished using this class, delete it by calling the <a href="https://msdn.microsoft.com/a2794f8f-a69a-49f3-8d7e-512c80ea782b">MI_Class_Delete</a> function.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



<b>MI_Class_Clone</b> may not create a whole new class; instead, it may refer to the original class.  Each class can be closed independent of the other, but not all of the memory is freed until all references to the class are deleted.



