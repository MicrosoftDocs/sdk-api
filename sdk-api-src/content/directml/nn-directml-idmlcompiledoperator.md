---
UID: NN:directml.IDMLCompiledOperator
title: IDMLCompiledOperator
description: Represents a compiled, efficient form of an operator suitable for execution on the GPU. To create this object, call IDMLDevice::CompileOperator.
helpviewer_keywords: ["IDMLCompiledOperator","IDMLCompiledOperator interface","IDMLCompiledOperator interface","described","direct3d12.idmlcompiledoperator","directml/IDMLCompiledOperator"]
old-location: direct3d12\idmlcompiledoperator.htm
tech.root: directml
ms.assetid: B8819F85-CF53-428C-806F-2B3B61D5D869
ms.date: 12/5/2018
ms.keywords: IDMLCompiledOperator, IDMLCompiledOperator interface, IDMLCompiledOperator interface,described, direct3d12.idmlcompiledoperator, directml/IDMLCompiledOperator
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
 - IDMLCompiledOperator
 - directml/IDMLCompiledOperator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLCompiledOperator
---

# IDMLCompiledOperator interface


## -description

Represents a compiled, efficient form of an operator suitable for execution on the GPU. To create this object, call [IDMLDevice::CompileOperator](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator). The **IDMLCompiledOperator** interface inherits from [IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable).

Unlike [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator), compiled operators are "baked", and can be executed directly by the GPU. After an operator is
    compiled, you must initialize it exactly once before it can be executed. It's an error to initialize an
    operator more than once. Operator initializers are used to initialize compiled operators.
    You can use [IDMLCommandRecorder::RecordDispatch](/windows/win32/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) to record the dispatch of an operator initializer which, when
    executed on the GPU, will initialize one or more operators.

In addition to input and output tensors, operators may require additional memory for execution. This
    additional memory must be provided by your application in the form of temporary and persistent resources.

A temporary resource is scratch memory that is only used during the execution of the operator, and doesn't
    need to persist after the call to [IDMLCommandRecorder::RecordDispatch](/windows/win32/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) completes on the GPU. This means that your
    application may release or overwrite the temporary resource in between dispatches of the compiled operator. In
    contrast, the persistent resource must live at least until the last execute of the operator has completed on
    the GPU. Additionally, the contents of the persistent resource are opaque and must be preserved between executions
    of the operator.

The size of the temporary and persistent resources varies per operator. Call
    [IDMLDispatchable::GetBindingProperties](/windows/win32/api/directml/nf-directml-idmldispatchable-getbindingproperties) to query the required size, in bytes, of the persistent and temporary
    resources for this compiled operator. See <a href="/windows/win32/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource">IDMLBindingTable::BindTemporaryResource</a> and
    <a href="/windows/win32/api/directml/nf-directml-idmlbindingtable-bindpersistentresource">IDMLBindingTable::BindPersistentResource</a> for more information on binding temporary and persistent resources.

All methods on this interface are thread-safe.

## -see-also

[Binding in DirectML](/windows/ai/directml/dml-binding)

[IDMLDispatchable](/windows/win32/api/directml/nn-directml-idmldispatchable)
