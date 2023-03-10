---
UID: NF:mi.MI_OperationOptions_GetString
title: MI_OperationOptions_GetString function (mi.h)
description: Gets a custom string option.
helpviewer_keywords: ["MI_OperationOptions_GetString","MI_OperationOptions_GetString function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetString","wmi_v2.mi_operationoptions_getstring"]
old-location: wmi_v2\mi_operationoptions_getstring.htm
tech.root: wmi_v2
ms.assetid: 1d1b9650-10c3-4e06-a841-6706ecc5f32c
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetString, MI_OperationOptions_GetString function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetString, wmi_v2.mi_operationoptions_getstring
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
 - MI_OperationOptions_GetString
 - mi/MI_OperationOptions_GetString
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
 - MI_OperationOptions_GetString
---

# MI_OperationOptions_GetString function


## -description

Gets a custom string option.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param optionName

A null-terminated string that represents the name of the option.

### -param value

Returned option value.

### -param index [out, optional]

Returned zero-based index of the option.

### -param flags [out, optional]

Returned option flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setstring">MI_OperationOptions_SetString</a>