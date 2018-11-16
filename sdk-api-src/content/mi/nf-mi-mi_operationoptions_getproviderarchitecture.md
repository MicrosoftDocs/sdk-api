---
UID: NF:mi.MI_OperationOptions_GetProviderArchitecture
title: MI_OperationOptions_GetProviderArchitecture function
author: windows-sdk-content
description: Gets the provider architecture for an operation.
old-location: wmi_v2\mi_operationoptions_getproviderarchitecture.htm
tech.root: wmi_v2
ms.assetid: a9994178-0f42-4f4c-9236-42e993d9d86c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MI_OperationOptions_GetProviderArchitecture, MI_OperationOptions_GetProviderArchitecture function [Windows Management Infrastructure (MI)], MI_PROVIDER_ARCHITECTURE_32BIT, MI_PROVIDER_ARCHITECTURE_64BIT, mi/MI_OperationOptions_GetProviderArchitecture, wmi_v2.mi_operationoptions_getproviderarchitecture
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_GetProviderArchitecture
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
- apiref
: 
- 
: 
- MI_OperationOptions_GetProviderArchitecture
: 
---

# MI_OperationOptions_GetProviderArchitecture function


## -description


Gets the provider architecture for an operation.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param architecture [out]

Returned MI_ProviderArchitecture value.



#### MI_PROVIDER_ARCHITECTURE_32BIT

32-bit architecture.



#### MI_PROVIDER_ARCHITECTURE_64BIT

64-bit architecture.


### -param mustComply [out]

Returned Boolean value where <b>MI_TRUE</b> means that if you are asking for a 32-bit provider on a 64-bit machine, then a 32-bit provider must be used.


## -returns



This function returns MI_INLINE MI_Result.



