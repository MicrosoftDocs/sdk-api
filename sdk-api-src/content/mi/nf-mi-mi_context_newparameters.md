---
UID: NF:mi.MI_Context_NewParameters
title: MI_Context_NewParameters function
author: windows-sdk-content
description: Creates a new instance of a method given a method declaration.
old-location: wmi_v2\mi_context_newparameters.htm
old-project: wmi_v2
ms.assetid: 8fb80e6f-627c-4897-9776-7454c0258809
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_Context_NewParameters, MI_Context_NewParameters function [Windows Management Infrastructure (MI)], mi/MI_Context_NewParameters, wmi.mi_newparameters, wmi_v2.mi_context_newparameters
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
-	MI_Context_NewParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Context_NewParameters function


## -description


Creates a new instance of a method given a method declaration.


## -parameters




### -param context [in]

A pointer to the request context.


### -param methodDecl [in]

A pointer to the Method declaration used to initialize the instance.


### -param instance

A pointer to the returned instance.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



When you are finished using the instance, it must be deleted with the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.



