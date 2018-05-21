---
UID: NF:mi.MI_Instance_ClearElementAt
title: MI_Instance_ClearElementAt function
author: windows-driver-content
description: Clears the value of the element (CIM property) at the specified index and sets it to NULL.
old-location: wmi_v2\mi_instance_clearelementat.htm
old-project: wmi_v2
ms.assetid: ef97bfa4-2e06-44b1-aa50-ce8c6a550c69
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_Instance_ClearElementAt, MI_Instance_ClearElementAt function [Windows Management Infrastructure (MI)], mi/MI_Instance_ClearElementAt, wmi_v2.mi_instance_clearelementat
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
-	MI_Instance_ClearElementAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_ClearElementAt function


## -description


Clears the value of the  element (CIM property) at the specified index and sets it to <b>NULL</b>.


## -parameters




### -param self [in, out]

Instance whose property will be set.


### -param index

Zero-based index of the element that will be set.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



