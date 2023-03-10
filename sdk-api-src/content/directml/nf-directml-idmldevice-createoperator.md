---
UID: NF:directml.IDMLDevice.CreateOperator
title: IDMLDevice::CreateOperator
description: Creates a DirectML operator.
helpviewer_keywords: ["CreateOperator","CreateOperator method","CreateOperator method","IDMLDevice interface","IDMLDevice interface","CreateOperator method","IDMLDevice.CreateOperator","IDMLDevice::CreateOperator","direct3d12.idmldevice_createoperator","directml/IDMLDevice::CreateOperator"]
old-location: direct3d12\idmldevice_createoperator.htm
tech.root: directml
ms.assetid: BAD28B3F-6F7C-45A0-9604-0660FF367878
ms.date: 12/5/2018
ms.keywords: CreateOperator, CreateOperator method, CreateOperator method,IDMLDevice interface, IDMLDevice interface,CreateOperator method, IDMLDevice.CreateOperator, IDMLDevice::CreateOperator, direct3d12.idmldevice_createoperator, directml/IDMLDevice::CreateOperator
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
 - IDMLDevice::CreateOperator
 - directml/IDMLDevice::CreateOperator
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
 - IDMLDevice.CreateOperator
---

# IDMLDevice::CreateOperator


## -description

Creates a DirectML operator.

In DirectML, an operator represents an abstract bundle of functionality, which can be compiled into a form suitable
        for execution on the GPU. Operator objects cannot be executed directly; they must first be compiled into an
        [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

## -parameters

### -param desc

Type: **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

The description of the operator to be created.

### -param riid

Type: <b>REFIID</b>

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>. This is expected to be the GUID of [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator).

### -param ppv [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the operator. This is the address of a pointer to an [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator), representing  the operator created.

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)

<a href="https://msdn.microsoft.com/745DB37D-20BF-4422-B224-A6BDEF272B8D">IDMLDevice::CompileOperator</a>
