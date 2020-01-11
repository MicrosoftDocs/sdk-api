---
UID: NS:mi._MI_OperationOptionsFT
title: MI_OperationOptionsFT (mi.h)
description: A support structure used in the MI_OperationOptions structure. Use the functions with the name prefix &#0034;MI_OperationOptions_&#0034; to manipulate these structures.
old-location: wmi_v2\mi_operationoptionsft.htm
tech.root: wmi_v2
ms.assetid: ed84d3bc-2cb0-4052-902d-96a3ab3a3ba4
ms.date: 12/05/2018
ms.keywords: MI_OperationOptionsFT, MI_OperationOptionsFT structure [Windows Management Infrastructure (MI)], mi/MI_OperationOptionsFT, wmi_v2.mi_operationoptionsft
f1_keywords:
- mi/MI_OperationOptionsFT
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_OperationOptionsFT
targetos: Windows
req.typenames: MI_OperationOptionsFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_OperationOptionsFT structure


## -description


A support structure used in the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.  Use the functions with the name prefix "MI_OperationOptions_" to manipulate these structures.


## -struct-fields




### -field MI_Result

TBD 




#### - Clone

Creates a copy of a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_clone">MI_OperationOptions_Clone</a>.


#### - Delete

Deletes an option and its associated memory. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_delete">MI_OperationOptions_Delete</a>.


#### - GetEnabledChannels

See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getenabledchannels">MI_OperationOptions_GetEnabledChannels</a>.


#### - GetNumber

Gets a previously added custom number option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getnumber">MI_OperationOptions_GetNumber</a>.


#### - GetOption

Gets a previously added option value based on the option name. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getoption">MI_OperationOptions_GetOption</a>.


#### - GetOptionAt

Gets a previously added option value based on the specified index. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getoptionat">MI_OperationOptions_GetOptionAt</a>.


#### - GetOptionCount

Gets the number of options previously added. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getoptioncount">MI_OperationOptions_GetOptionCount</a>.


#### - GetString

Gets a custom string option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_getstring">MI_OperationOptions_GetString</a>.


#### - SetCustomOption

Sets a custom option for the operation. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setcustomoption">MI_OperationOptions_SetCustomOption</a>.


#### - SetNumber

Sets a custom number option value. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setnumber">MI_OperationOptions_SetNumber</a>.


#### - SetString

Sets a custom string option. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_operationoptions_setstring">MI_OperationOptions_SetString</a>.

