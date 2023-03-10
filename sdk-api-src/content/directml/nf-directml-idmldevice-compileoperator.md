---
UID: NF:directml.IDMLDevice.CompileOperator
title: IDMLDevice::CompileOperator
description: Compiles an operator into an object that can be dispatched to the GPU.
helpviewer_keywords: ["CompileOperator","CompileOperator method","CompileOperator method","IDMLDevice interface","IDMLDevice interface","CompileOperator method","IDMLDevice.CompileOperator","IDMLDevice::CompileOperator","direct3d12.idmldevice_compileoperator","directml/IDMLDevice::CompileOperator"]
old-location: direct3d12\idmldevice_compileoperator.htm
tech.root: directml
ms.assetid: 745DB37D-20BF-4422-B224-A6BDEF272B8D
ms.date: 12/5/2018
ms.keywords: CompileOperator, CompileOperator method, CompileOperator method,IDMLDevice interface, IDMLDevice interface,CompileOperator method, IDMLDevice.CompileOperator, IDMLDevice::CompileOperator, direct3d12.idmldevice_compileoperator, directml/IDMLDevice::CompileOperator
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMLDevice::CompileOperator
 - directml/IDMLDevice::CompileOperator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLDevice.CompileOperator
---

# IDMLDevice::CompileOperator


## -description

Compiles an operator into an object that can be dispatched to the GPU.

A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.
        A compiled operator holds state (such as shaders and other objects) required for execution. Because a compiled operator
        implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish. See
        [IDMLDevice::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.

The compiled operator maintains a strong reference to the supplied [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) pointer.

## -parameters

### -param op

Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)*</b>

The operator (created with [IDMLDevice::CreateOperator](/windows/win32/api/directml/nf-directml-idmldevice-createoperator)) to compile.

### -param flags

Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Any flags to control the execution of this operator.

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the compiled operator. This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)
