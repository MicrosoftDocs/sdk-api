---
UID: NF:mi.MI_OperationOptions_GetOptionAt
title: MI_OperationOptions_GetOptionAt function (mi.h)
description: Gets a previously added option value based on the specified index. (MI_OperationOptions_GetOptionAt)
helpviewer_keywords: ["MI_OperationOptions_GetOptionAt","MI_OperationOptions_GetOptionAt function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetOptionAt","wmi_v2.mi_operationoptions_getoptionat"]
old-location: wmi_v2\mi_operationoptions_getoptionat.htm
tech.root: wmi_v2
ms.assetid: 06ae674b-c7d7-47c1-81f2-6a825d9889a2
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetOptionAt, MI_OperationOptions_GetOptionAt function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetOptionAt, wmi_v2.mi_operationoptions_getoptionat
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
 - MI_OperationOptions_GetOptionAt
 - mi/MI_OperationOptions_GetOptionAt
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
 - MI_OperationOptions_GetOptionAt
---

# MI_OperationOptions_GetOptionAt function


## -description

Gets a previously added option value based on the specified index.

## -parameters

### -param options [in]

MI_OperationOptions structure.

### -param index

Zero-based index of the option.

### -param optionName

Returned option name.

### -param value [out]

Returned option value.

### -param type [out]

Returned option type.

### -param flags [out, optional]

Returned option flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
