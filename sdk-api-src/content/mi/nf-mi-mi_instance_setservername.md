---
UID: NF:mi.MI_Instance_SetServerName
title: MI_Instance_SetServerName function
author: windows-driver-content
description: Sets the server name of the specified instance.
old-location: wmi_v2\mi_instance_setservername.htm
old-project: wmi_v2
ms.assetid: 34864c69-091f-4dbd-9d56-e43f8d218b09
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_Instance_SetServerName, MI_Instance_SetServerName function [Windows Management Infrastructure (MI)], mi/MI_Instance_SetServerName, wmi_v2.mi_instance_setservername
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
-	MI_Instance_SetServerName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_SetServerName function


## -description


Sets the server name of the specified instance.


## -parameters




### -param self [in, out]

Instance whose server name is to be set.


### -param name

A null-terminated string that represents the new server name.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



