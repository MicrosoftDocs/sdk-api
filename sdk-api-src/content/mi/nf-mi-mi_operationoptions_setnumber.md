---
UID: NF:mi.MI_OperationOptions_SetNumber
title: MI_OperationOptions_SetNumber function (mi.h)
description: Sets a custom number option value.
helpviewer_keywords: ["MI_OperationOptions_SetNumber","MI_OperationOptions_SetNumber function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_SetNumber","wmi_v2.mi_operationoptions_setnumber"]
old-location: wmi_v2\mi_operationoptions_setnumber.htm
tech.root: wmi_v2
ms.assetid: 2f357a9c-7e61-4f78-b4cc-2dd0a8259c3d
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_SetNumber, MI_OperationOptions_SetNumber function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_SetNumber, wmi_v2.mi_operationoptions_setnumber
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
 - MI_OperationOptions_SetNumber
 - mi/MI_OperationOptions_SetNumber
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
 - MI_OperationOptions_SetNumber
---

# MI_OperationOptions_SetNumber function


## -description

Sets a custom number option value.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param optionName

A null-terminated string that represents the name of the option to set.

### -param value [in]

New option value.

### -param flags

Option flags.

## -returns

This function returns MI_INLINE MI_Result.