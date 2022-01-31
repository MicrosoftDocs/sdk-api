---
UID: NE:directml.DML_EXECUTION_FLAGS
title: DML_EXECUTION_FLAGS
description: Supplies options to DirectML to control execution of operators. These flags can be bitwise OR'd together to specify multiple flags at once.
helpviewer_keywords: ["DML_EXECUTION_FLAGS","DML_EXECUTION_FLAGS enumeration","DML_EXECUTION_FLAG_ALLOW_HALF_PRECISION_COMPUTATION","DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE","DML_EXECUTION_FLAG_DISABLE_META_COMMANDS","DML_EXECUTION_FLAG_NONE","direct3d12.dml_execution_flags","directml/DML_EXECUTION_FLAGS","directml/DML_EXECUTION_FLAG_ALLOW_HALF_PRECISION_COMPUTATION","directml/DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE","directml/DML_EXECUTION_FLAG_DISABLE_META_COMMANDS","directml/DML_EXECUTION_FLAG_NONE"]
old-location: direct3d12\dml_execution_flags.htm
tech.root: directml
ms.assetid: 753E51EE-8739-4263-8257-FBC13718B71F
ms.date: 12/5/2018
ms.keywords: DML_EXECUTION_FLAGS, DML_EXECUTION_FLAGS enumeration, DML_EXECUTION_FLAG_ALLOW_HALF_PRECISION_COMPUTATION, DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE, DML_EXECUTION_FLAG_DISABLE_META_COMMANDS, DML_EXECUTION_FLAG_NONE, direct3d12.dml_execution_flags, directml/DML_EXECUTION_FLAGS, directml/DML_EXECUTION_FLAG_ALLOW_HALF_PRECISION_COMPUTATION, directml/DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE, directml/DML_EXECUTION_FLAG_DISABLE_META_COMMANDS, directml/DML_EXECUTION_FLAG_NONE
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - DML_EXECUTION_FLAGS
 - directml/DML_EXECUTION_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_EXECUTION_FLAGS
---

## -description

Supplies options to DirectML to control execution of operators. These flags can be bitwise OR'd together to specify multiple flags at once.

## -enum-fields

### -field DML_EXECUTION_FLAG_NONE:0

No execution flags are specified.

### -field DML_EXECUTION_FLAG_ALLOW_HALF_PRECISION_COMPUTATION:0x1

Allows DirectML to perform computation using half-precision floating-point (FP16), if supported by the hardware device.

### -field DML_EXECUTION_FLAG_DISABLE_META_COMMANDS:0x2

Forces DirectML execute the operator using DirectCompute instead of meta commands. DirectML uses meta commands by default, if available.

### -field DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE:0x4

Allows changes to bindings after an operator's execution has been recorded in a command list, but before it has been submitted to the command queue. By default, without this flag set, you must set all bindings on the binding table before you record an operator into a command list.

This flag allows you to perform late binding—that is, to set (or to change) bindings on operators that you've already recorded into a command list. However, this may result in a performance penalty on some hardware, as it prohibits drivers from promoting static descriptor accesses to root descriptor accesses.

For more info, see <a href="/windows/win32/direct3d12/root-signature-version-1-1#descriptors_volatile">DESCRIPTORS_VOLATILE</a>.

## -see-also

<a href="/windows/ai/directml/dml-binding">Binding in DirectML</a>
