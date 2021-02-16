---
UID: NS:mi._MI_OperationOptionsFT
title: MI_OperationOptionsFT (mi.h)
description: A support structure used in the MI_OperationOptions structure. Use the functions with the name prefix &quot;MI_OperationOptions_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_OperationOptionsFT","MI_OperationOptionsFT structure [Windows Management Infrastructure (MI)]","mi/MI_OperationOptionsFT","wmi_v2.mi_operationoptionsft"]
old-location: wmi_v2\mi_operationoptionsft.htm
tech.root: wmi_v2
ms.assetid: ed84d3bc-2cb0-4052-902d-96a3ab3a3ba4
ms.date: 12/05/2018
ms.keywords: MI_OperationOptionsFT, MI_OperationOptionsFT structure [Windows Management Infrastructure (MI)], mi/MI_OperationOptionsFT, wmi_v2.mi_operationoptionsft
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
req.typenames: MI_OperationOptionsFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_OperationOptionsFT
 - mi/_MI_OperationOptionsFT
 - MI_OperationOptionsFT
 - mi/MI_OperationOptionsFT
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
 - MI_OperationOptionsFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.  Use the functions with the name prefix "MI_OperationOptions_" to manipulate these structures.

## -struct-fields

### -field Clone

Creates a copy of a <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_clone">MI_OperationOptions_Clone</a>.

### -field Delete

Deletes an option and its associated memory. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_delete">MI_OperationOptions_Delete</a>.

### -field GetEnabledChannels

See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getenabledchannels">MI_OperationOptions_GetEnabledChannels</a>.

### -field GetNumber

Gets a previously added custom number option. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getnumber">MI_OperationOptions_GetNumber</a>.

### -field GetOption

Gets a previously added option value based on the option name. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getoption">MI_OperationOptions_GetOption</a>.

### -field GetOptionAt

Gets a previously added option value based on the specified index. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getoptionat">MI_OperationOptions_GetOptionAt</a>.

### -field GetOptionCount

Gets the number of options previously added. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getoptioncount">MI_OperationOptions_GetOptionCount</a>.

### -field GetString

Gets a custom string option. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getstring">MI_OperationOptions_GetString</a>.

### -field SetCustomOption

Sets a custom option for the operation. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setcustomoption">MI_OperationOptions_SetCustomOption</a>.

### -field SetNumber

Sets a custom number option value. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setnumber">MI_OperationOptions_SetNumber</a>.

### -field SetString

Sets a custom string option. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setstring">MI_OperationOptions_SetString</a>.

### -field SetInterval

TBD

### -field GetInterval

TBD
