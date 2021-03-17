---
UID: NF:mi.MI_OperationOptions_GetResourceUriPrefix
title: MI_OperationOptions_GetResourceUriPrefix function (mi.h)
description: Gets the resource URI prefix being used for an operation.
helpviewer_keywords: ["MI_OperationOptions_GetResourceUriPrefix","MI_OperationOptions_GetResourceUriPrefix function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetResourceUriPrefix","wmi_v2.mi_operationoptions_getresourceuriprefix"]
old-location: wmi_v2\mi_operationoptions_getresourceuriprefix.htm
tech.root: wmi_v2
ms.assetid: c6ef1e8c-0d80-4359-a0f4-9d25ed39eae3
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetResourceUriPrefix, MI_OperationOptions_GetResourceUriPrefix function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetResourceUriPrefix, wmi_v2.mi_operationoptions_getresourceuriprefix
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
 - MI_OperationOptions_GetResourceUriPrefix
 - mi/MI_OperationOptions_GetResourceUriPrefix
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
 - MI_OperationOptions_GetResourceUriPrefix
---

# MI_OperationOptions_GetResourceUriPrefix function


## -description

Gets the resource URI prefix being used for an operation.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param ruriPrefix

Returned resource URI being used for the operation.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.