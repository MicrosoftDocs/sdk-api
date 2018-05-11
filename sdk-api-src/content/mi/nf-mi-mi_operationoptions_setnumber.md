---
UID: NF:mi.MI_OperationOptions_SetNumber
title: MI_OperationOptions_SetNumber function
author: windows-driver-content
description: Sets a custom number option value.
old-location: wmi_v2\mi_operationoptions_setnumber.htm
old-project: wmi_v2
ms.assetid: 2f357a9c-7e61-4f78-b4cc-2dd0a8259c3d
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_OperationOptions_SetNumber, MI_OperationOptions_SetNumber function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetNumber, wmi_v2.mi_operationoptions_setnumber
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
-	MI_OperationOptions_SetNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetNumber function


## -description


Sets a custom number option value.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param optionName

A null-terminated string that represents the name of the option to set.


### -param value [in]

New option value.


### -param flags

Option flags.


## -returns



This function returns MI_INLINE MI_Result.



