---
UID: NF:mi.MI_OperationOptions_SetCustomOption
title: MI_OperationOptions_SetCustomOption function (mi.h)
description: Sets a custom option for the operation.
helpviewer_keywords: ["MI_OperationOptions_SetCustomOption","MI_OperationOptions_SetCustomOption function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_SetCustomOption","wmi_v2.mi_operationoptions_setcustomoption"]
old-location: wmi_v2\mi_operationoptions_setcustomoption.htm
tech.root: wmi_v2
ms.assetid: 5db96e9e-dd81-4b62-a555-770b781d0ed3
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetCustomOption, MI_OperationOptions_SetCustomOption function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetCustomOption, wmi_v2.mi_operationoptions_setcustomoption
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
 - MI_OperationOptions_SetCustomOption
 - mi/MI_OperationOptions_SetCustomOption
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
 - MI_OperationOptions_SetCustomOption
---

# MI_OperationOptions_SetCustomOption function


## -description

Sets a  custom option for the operation.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param optionName

A null-terminated string that represents the name of the option to set.

### -param optionValueType [in]

Option type.

### -param optionValue [in]

New option value.

### -param mustComply

Boolean value where <b>MI_TRUE</b> means that the option must be complied with.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.