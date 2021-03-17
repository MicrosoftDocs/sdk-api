---
UID: NF:mi.MI_OperationOptions_GetProviderArchitecture
title: MI_OperationOptions_GetProviderArchitecture function (mi.h)
description: Gets the provider architecture for an operation.
helpviewer_keywords: ["MI_OperationOptions_GetProviderArchitecture","MI_OperationOptions_GetProviderArchitecture function [Windows Management Infrastructure (MI)]","MI_PROVIDER_ARCHITECTURE_32BIT","MI_PROVIDER_ARCHITECTURE_64BIT","mi/MI_OperationOptions_GetProviderArchitecture","wmi_v2.mi_operationoptions_getproviderarchitecture"]
old-location: wmi_v2\mi_operationoptions_getproviderarchitecture.htm
tech.root: wmi_v2
ms.assetid: a9994178-0f42-4f4c-9236-42e993d9d86c
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetProviderArchitecture, MI_OperationOptions_GetProviderArchitecture function [Windows Management Infrastructure (MI)], MI_PROVIDER_ARCHITECTURE_32BIT, MI_PROVIDER_ARCHITECTURE_64BIT, mi/MI_OperationOptions_GetProviderArchitecture, wmi_v2.mi_operationoptions_getproviderarchitecture
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_OperationOptions_GetProviderArchitecture
 - mi/MI_OperationOptions_GetProviderArchitecture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_GetProviderArchitecture
---

# MI_OperationOptions_GetProviderArchitecture function


## -description

Gets the provider architecture for an operation.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

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