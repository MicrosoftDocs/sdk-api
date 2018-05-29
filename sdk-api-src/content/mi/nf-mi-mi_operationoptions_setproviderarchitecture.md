---
UID: NF:mi.MI_OperationOptions_SetProviderArchitecture
title: MI_OperationOptions_SetProviderArchitecture function
author: windows-sdk-content
description: Sets the provider architecture for an operation.
old-location: wmi_v2\mi_operationoptions_setproviderarchitecture.htm
old-project: wmi_v2
ms.assetid: 70caef27-577c-4fa0-9c9e-c9724750b136
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_OperationOptions_SetProviderArchitecture, MI_OperationOptions_SetProviderArchitecture function [Windows Management Infrastructure (MI)], MI_PROVIDER_ARCHITECTURE_32BIT, MI_PROVIDER_ARCHITECTURE_64BIT, mi/MI_OperationOptions_SetProviderArchitecture, wmi_v2.mi_operationoptions_setproviderarchitecture
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
-	MI_OperationOptions_SetProviderArchitecture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_SetProviderArchitecture function


## -description


Sets the provider architecture for an operation.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param architecture [in]

One of the following <a href="https://msdn.microsoft.com/9dd275aa-23a9-44f4-916f-355b77490161">MI_ProviderArchitecture</a> values.



#### MI_PROVIDER_ARCHITECTURE_32BIT (0)

32-bit architecture.



#### MI_PROVIDER_ARCHITECTURE_64BIT (1)

64-bit architecture.


### -param mustComply [in]

Boolean value where <b>MI_TRUE</b> means that if you are asking for a 32-bit provider on a 64-bit machine, then a 32-bit provider must be used.  <b>MI_FALSE</b> means that a 64-bit provider can be used if a 32-bit provider is not available.


## -returns



This function returns MI_INLINE MI_Result.



