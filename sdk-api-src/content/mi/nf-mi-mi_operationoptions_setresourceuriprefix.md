---
UID: NF:mi.MI_OperationOptions_SetResourceUriPrefix
title: MI_OperationOptions_SetResourceUriPrefix function (mi.h)
description: Sets the resource URI prefix to use for an operation.
helpviewer_keywords: ["MI_OperationOptions_SetResourceUriPrefix","MI_OperationOptions_SetResourceUriPrefix function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_SetResourceUriPrefix","wmi_v2.mi_operationoptions_setresourceuriprefix"]
old-location: wmi_v2\mi_operationoptions_setresourceuriprefix.htm
tech.root: wmi_v2
ms.assetid: 7f384720-7673-4dd2-883f-a52da4a51729
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetResourceUriPrefix, MI_OperationOptions_SetResourceUriPrefix function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetResourceUriPrefix, wmi_v2.mi_operationoptions_setresourceuriprefix
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
 - MI_OperationOptions_SetResourceUriPrefix
 - mi/MI_OperationOptions_SetResourceUriPrefix
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
 - MI_OperationOptions_SetResourceUriPrefix
---

# MI_OperationOptions_SetResourceUriPrefix function


## -description

Sets the resource URI prefix to use for an operation.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param ruriPrefix

A null-terminated string that represents the resource URI to use for the operation.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getresourceuriprefix">MI_OperationOptions_GetResourceUriPrefix</a>