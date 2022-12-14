---
UID: NE:directml.DML_CREATE_DEVICE_FLAGS
title: DML_CREATE_DEVICE_FLAGS
description: Supplies additional device creation options to DMLCreateDevice. Values can be bitwise OR'd together.
helpviewer_keywords: ["DML_CREATE_DEVICE_FLAGS","DML_CREATE_DEVICE_FLAGS enumeration","DML_CREATE_DEVICE_FLAG_DEBUG","DML_CREATE_DEVICE_FLAG_NONE","direct3d12.dml_create_device_flags","directml/DML_CREATE_DEVICE_FLAGS","directml/DML_CREATE_DEVICE_FLAG_DEBUG","directml/DML_CREATE_DEVICE_FLAG_NONE"]
old-location: direct3d12\dml_create_device_flags.htm
tech.root: directml
ms.assetid: 450D86CC-CC26-4926-8957-B0054C548801
ms.date: 12/5/2018
ms.keywords: DML_CREATE_DEVICE_FLAGS, DML_CREATE_DEVICE_FLAGS enumeration, DML_CREATE_DEVICE_FLAG_DEBUG, DML_CREATE_DEVICE_FLAG_NONE, direct3d12.dml_create_device_flags, directml/DML_CREATE_DEVICE_FLAGS, directml/DML_CREATE_DEVICE_FLAG_DEBUG, directml/DML_CREATE_DEVICE_FLAG_NONE
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
 - DML_CREATE_DEVICE_FLAGS
 - directml/DML_CREATE_DEVICE_FLAGS
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
 - DML_CREATE_DEVICE_FLAGS
---

## -description

Supplies additional device creation options to [DMLCreateDevice](/windows/win32/api/directml/nf-directml-dmlcreatedevice). Values can be bitwise OR'd together.

## -enum-fields

### -field DML_CREATE_DEVICE_FLAG_NONE:0

No creation options are specified.

### -field DML_CREATE_DEVICE_FLAG_DEBUG:0x1

Enables the DirectML debug layers. To use the debug layers, developer mode must be enabled, and the DirectML debug layers must be installed. If the <b>DML_CREATE_DEVICE_FLAG_DEBUG</b> flag is specified and either condition is not met, then [DMLCreateDevice](/windows/win32/api/directml/nf-directml-dmlcreatedevice) returns <b>DXGI_ERROR_SDK_COMPONENT_MISSING</b>.
