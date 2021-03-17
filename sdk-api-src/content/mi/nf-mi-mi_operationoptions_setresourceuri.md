---
UID: NF:mi.MI_OperationOptions_SetResourceUri
title: MI_OperationOptions_SetResourceUri function (mi.h)
description: Sets the resource URI to use for an operation.
helpviewer_keywords: ["MI_OperationOptions_SetResourceUri","MI_OperationOptions_SetResourceUri function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_SetResourceUri","wmi_v2.mi_operationoptions_setresourceuri"]
old-location: wmi_v2\mi_operationoptions_setresourceuri.htm
tech.root: wmi_v2
ms.assetid: 0722bc88-59a6-476b-a325-343d0eb43086
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetResourceUri, MI_OperationOptions_SetResourceUri function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetResourceUri, wmi_v2.mi_operationoptions_setresourceuri
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
req.lib: Mi.lib
req.dll: Mi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MI_OperationOptions_SetResourceUri
 - mi/MI_OperationOptions_SetResourceUri
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mi.dll
api_name:
 - MI_OperationOptions_SetResourceUri
---

# MI_OperationOptions_SetResourceUri function


## -description

Sets the resource URI to use for an operation.

## -parameters

### -param options [in, out]

A <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure containing a set of operation options.

### -param rUri [in]

A null-terminated string that represents the resource URI to use for the operation.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.