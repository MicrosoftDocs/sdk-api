---
UID: NF:mi.MI_Instance_ClearElement
title: MI_Instance_ClearElement function
author: windows-driver-content
description: Clears the value of the named element (CIM property) and sets it to NULL.
old-location: wmi_v2\mi_instance_clearelement.htm
old-project: wmi_v2
ms.assetid: de945902-4b10-47d1-a374-a1aeab02a787
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Instance_ClearElement, MI_Instance_ClearElement function [Windows Management Infrastructure (MI)], mi/MI_Instance_ClearElement, wmi_v2.mi_instance_clearelement
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
-	MI_Instance_ClearElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_ClearElement function


## -description


Clears the value of the named element (CIM property) and sets it to <b>NULL</b>.


## -parameters




### -param self [in, out]

Instance whose property will be set.


### -param name

A null-terminated string that represents the name of the property that will be cleared.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a>



<a href="https://msdn.microsoft.com/1e366cc5-0fb9-41c9-961c-07b076a18529">MI_Instance_GetElement</a>



<a href="https://msdn.microsoft.com/581f8d9f-5421-44ab-a3e2-dfb536a35c2c">MI_Instance_SetElement</a>
 

 

