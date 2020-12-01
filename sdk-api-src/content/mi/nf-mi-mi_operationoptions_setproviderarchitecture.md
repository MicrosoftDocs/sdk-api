---
UID: NF:mi.MI_OperationOptions_SetProviderArchitecture
title: MI_OperationOptions_SetProviderArchitecture function (mi.h)
description: Sets the provider architecture for an operation.
helpviewer_keywords: ["MI_OperationOptions_SetProviderArchitecture","MI_OperationOptions_SetProviderArchitecture function [Windows Management Infrastructure (MI)]","MI_PROVIDER_ARCHITECTURE_32BIT","MI_PROVIDER_ARCHITECTURE_64BIT","mi/MI_OperationOptions_SetProviderArchitecture","wmi_v2.mi_operationoptions_setproviderarchitecture"]
old-location: wmi_v2\mi_operationoptions_setproviderarchitecture.htm
tech.root: wmi_v2
ms.assetid: 70caef27-577c-4fa0-9c9e-c9724750b136
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetProviderArchitecture, MI_OperationOptions_SetProviderArchitecture function [Windows Management Infrastructure (MI)], MI_PROVIDER_ARCHITECTURE_32BIT, MI_PROVIDER_ARCHITECTURE_64BIT, mi/MI_OperationOptions_SetProviderArchitecture, wmi_v2.mi_operationoptions_setproviderarchitecture
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
 - MI_OperationOptions_SetProviderArchitecture
 - mi/MI_OperationOptions_SetProviderArchitecture
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
 - MI_OperationOptions_SetProviderArchitecture
---

# MI_OperationOptions_SetProviderArchitecture function


## -description

Sets the provider architecture for an operation.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param architecture [in]

One of the following <a href="/windows/desktop/api/mi/ne-mi-mi_providerarchitecture">MI_ProviderArchitecture</a> values.



#### MI_PROVIDER_ARCHITECTURE_32BIT (0)

32-bit architecture.



#### MI_PROVIDER_ARCHITECTURE_64BIT (1)

64-bit architecture.

### -param mustComply [in]

Boolean value where <b>MI_TRUE</b> means that if you are asking for a 32-bit provider on a 64-bit machine, then a 32-bit provider must be used.  <b>MI_FALSE</b> means that a 64-bit provider can be used if a 32-bit provider is not available.

## -returns

This function returns MI_INLINE MI_Result.