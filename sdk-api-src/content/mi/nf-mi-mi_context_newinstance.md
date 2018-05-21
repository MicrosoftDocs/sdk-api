---
UID: NF:mi.MI_Context_NewInstance
title: MI_Context_NewInstance function
author: windows-driver-content
description: Creates a new instance of a class given a class declaration.
old-location: wmi_v2\mi_context_newinstance.htm
old-project: wmi_v2
ms.assetid: 59571aa0-7fc2-4724-94e8-15b8a62327b6
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_Context_NewInstance, MI_Context_NewInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_NewInstance, wmi.mi_newinstance, wmi_v2.mi_context_newinstance
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
-	MI_Context_NewInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_NewInstance function


## -description


Creates a new instance of a class given a class declaration.


## -parameters




### -param context [in]

A pointer to the request context.


### -param classDecl [in]

A pointer to the class declaration used to initialize the instance. The runtime type information (RTTI) is generated for the class and should be named for the class, followed by an "_rtti" suffix.


### -param instance

A pointer to the returned instance. There is also a generated function named for the class, followed by a  "_Delete" suffix.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



When you are finished using the instance, it must be deleted via the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.



