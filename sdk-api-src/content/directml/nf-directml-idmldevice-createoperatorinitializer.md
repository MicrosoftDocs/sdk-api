---
UID: NF:directml.IDMLDevice.CreateOperatorInitializer
title: IDMLDevice::CreateOperatorInitializer
description: Creates an object that can be used to initialize compiled operators.
helpviewer_keywords: ["CreateOperatorInitializer","CreateOperatorInitializer method","CreateOperatorInitializer method","IDMLDevice interface","IDMLDevice interface","CreateOperatorInitializer method","IDMLDevice.CreateOperatorInitializer","IDMLDevice::CreateOperatorInitializer","direct3d12.idmldevice_createoperatorinitializer","directml/IDMLDevice::CreateOperatorInitializer"]
old-location: direct3d12\idmldevice_createoperatorinitializer.htm
tech.root: directml
ms.assetid: B7047026-F176-494E-90A5-2C6085A5D027
ms.date: 12/5/2018
ms.keywords: CreateOperatorInitializer, CreateOperatorInitializer method, CreateOperatorInitializer method,IDMLDevice interface, IDMLDevice interface,CreateOperatorInitializer method, IDMLDevice.CreateOperatorInitializer, IDMLDevice::CreateOperatorInitializer, direct3d12.idmldevice_createoperatorinitializer, directml/IDMLDevice::CreateOperatorInitializer
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
 - IDMLDevice::CreateOperatorInitializer
 - directml/IDMLDevice::CreateOperatorInitializer
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
 - IDMLDevice.CreateOperatorInitializer
---

# IDMLDevice::CreateOperatorInitializer


## -description

Creates an object that can be used to initialize compiled operators.

Once compiled, an operator must be
        initialized exactly once on the GPU before it can be executed. The operator initializer holds the state
        necessary for initialization of one or more target compiled operators.

Once instantiated, dispatch of the operator initializer can be recorded in a command list via
        [IDMLCommandRecorder::RecordDispatch](/windows/win32/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). After execution completes on the GPU, all compiled operators that are
        targets of the initializer enter the initialized state.

An operator initializer can be reused to initialize different sets of compiled operators. See
        [IDMLOperatorInitializer::Reset](/windows/win32/api/directml/nf-directml-idmloperatorinitializer-reset) for more info.

An operator initializer can be created with no target operators. Executing such an initializer is a no-op.
        Creating an operator initializer with no target operators may be useful if you wish to create an initializer
        up-front, but don't yet know which operators it will be used to initialize. [IDMLOperatorInitializer::Reset](/windows/win32/api/directml/nf-directml-idmloperatorinitializer-reset) can be used to reset which
        operators to target.

## -parameters

### -param operatorCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This parameter determines the number of elements in the array passed in the  <i>operators</i> parameter.

### -param operators [in, optional]

Type: <b>[IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)*</b>

An optional pointer to a constant array of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator) pointers containing the set of operators that this initializer will target. Upon execution of the initializer, the target
          operators become initialized. This array may be null or empty, indicating that the initializer has no target
          operators.

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer).

### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the operator initializer. This is the address of a pointer to an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), representing  the operator initializer created.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)
