---
UID: NF:mi.MI_OperationOptions_GetResourceUri
title: MI_OperationOptions_GetResourceUri function (mi.h)
description: Gets the resource URI being used for an operation.
helpviewer_keywords: ["MI_OperationOptions_GetResourceUri","MI_OperationOptions_GetResourceUri function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetResourceUri","wmi_v2.mi_operationoptions_getresourceuri"]
old-location: wmi_v2\mi_operationoptions_getresourceuri.htm
tech.root: wmi_v2
ms.assetid: 24aff5ba-21e9-496c-a28d-7daeda26b670
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetResourceUri, MI_OperationOptions_GetResourceUri function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetResourceUri, wmi_v2.mi_operationoptions_getresourceuri
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
 - MI_OperationOptions_GetResourceUri
 - mi/MI_OperationOptions_GetResourceUri
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
 - MI_OperationOptions_GetResourceUri
---

# MI_OperationOptions_GetResourceUri function


## -description

Gets the resource URI being used for an operation.

## -parameters

### -param options [in]

A <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure containing a set of operation options.

### -param rUri [out]

Returned resource URI being used for the operation.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.