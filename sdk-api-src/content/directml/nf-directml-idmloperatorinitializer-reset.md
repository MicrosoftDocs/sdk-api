---
UID: NF:directml.IDMLOperatorInitializer.Reset
title: IDMLOperatorInitializer::Reset
description: Resets the initializer to handle initialization of a new set of operators.
helpviewer_keywords: ["IDMLOperatorInitializer interface","Reset method","IDMLOperatorInitializer.Reset","IDMLOperatorInitializer::Reset","Reset","Reset method","Reset method","IDMLOperatorInitializer interface","direct3d12.idmloperatorinitializer_reset","directml/IDMLOperatorInitializer::Reset"]
old-location: direct3d12\idmloperatorinitializer_reset.htm
tech.root: directml
ms.assetid: 4C402D7D-C235-4807-BA84-44CC8FEE84F1
ms.date: 12/5/2018
ms.keywords: IDMLOperatorInitializer interface,Reset method, IDMLOperatorInitializer.Reset, IDMLOperatorInitializer::Reset, Reset, Reset method, Reset method,IDMLOperatorInitializer interface, direct3d12.idmloperatorinitializer_reset, directml/IDMLOperatorInitializer::Reset
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
 - IDMLOperatorInitializer::Reset
 - directml/IDMLOperatorInitializer::Reset
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
 - IDMLOperatorInitializer.Reset
---

# IDMLOperatorInitializer::Reset


## -description

Resets the initializer to handle initialization of a new set of operators.

You may use an initializer only to initialize a fixed set of operators, which are provided either during creation
        ([IDMLDevice::CreateOperatorInitializer](/windows/win32/api/directml/nf-directml-idmldevice-createoperatorinitializer)), or when the initializer is reset. Resetting the initializer allows your
        application to reuse an existing initializer object to initialize a new set of operators.

You must not call <b>Reset</b> until all outstanding work using the initializer has completed execution on the GPU.

This method is not thread-safe.

## -parameters

### -param operatorCount

Type: <b>UINT</b>

This parameter determines the number of elements in the array passed in the  <i>operators</i> parameter.

### -param operators [in, optional]

Type: <b>[IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)*</b>

An optional pointer to a constant array of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator) pointers containing the operators that the initializer should initialize.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)
