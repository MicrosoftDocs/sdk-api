---
UID: NE:avrfsdk.eHANDLE_TRACE_OPERATIONS
title: eHANDLE_TRACE_OPERATIONS (avrfsdk.h)
description: Identifies the type of handle operation that has occurred.
helpviewer_keywords: ["OperationDbBADREF","OperationDbCLOSE","OperationDbOPEN","OperationDbUnused","avrfsdk/OperationDbBADREF","avrfsdk/OperationDbCLOSE","avrfsdk/OperationDbOPEN","avrfsdk/OperationDbUnused","avrfsdk/eHANDLE_TRACE_OPERATIONS","base.ehandle_trace_operations","eHANDLE_TRACE_OPERATIONS","eHANDLE_TRACE_OPERATIONS enumeration [Windows API]","winprog.ehandle_trace_operations"]
old-location: winprog\ehandle_trace_operations.htm
tech.root: winprog
ms.assetid: bcaaa52a-8eb1-4ad7-9ee5-97cca91a2238
ms.date: 12/05/2018
ms.keywords: OperationDbBADREF, OperationDbCLOSE, OperationDbOPEN, OperationDbUnused, avrfsdk/OperationDbBADREF, avrfsdk/OperationDbCLOSE, avrfsdk/OperationDbOPEN, avrfsdk/OperationDbUnused, avrfsdk/eHANDLE_TRACE_OPERATIONS, base.ehandle_trace_operations, eHANDLE_TRACE_OPERATIONS, eHANDLE_TRACE_OPERATIONS enumeration [Windows API], winprog.ehandle_trace_operations
req.header: avrfsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eHANDLE_TRACE_OPERATIONS
 - avrfsdk/eHANDLE_TRACE_OPERATIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Avrfsdk.h
api_name:
 - eHANDLE_TRACE_OPERATIONS
---

# eHANDLE_TRACE_OPERATIONS enumeration


## -description

Identifies the type of handle operation that has occurred.

## -enum-fields

### -field OperationDbUnused

Not used at this time.

### -field OperationDbOPEN

Specifies an open (create) handle operation.

### -field OperationDbCLOSE

Specifies a close handle operation.

### -field OperationDbBADREF

Specifies an invalid handle operation.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>