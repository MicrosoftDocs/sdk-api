---
UID: NN:directml.IDMLDispatchable
title: IDMLDispatchable
description: Implemented by objects that can be recorded into a command list for dispatch on the GPU, using IDMLCommandRecorder::RecordDispatch.
helpviewer_keywords: ["IDMLDispatchable","IDMLDispatchable interface","IDMLDispatchable interface","described","direct3d12.idmldispatchable","directml/IDMLDispatchable"]
old-location: direct3d12\idmldispatchable.htm
tech.root: directml
ms.assetid: 4CE57EB6-0738-4A5B-84FE-9761363F304B
ms.date: 12/5/2018
ms.keywords: IDMLDispatchable, IDMLDispatchable interface, IDMLDispatchable interface,described, direct3d12.idmldispatchable, directml/IDMLDispatchable
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
 - IDMLDispatchable
 - directml/IDMLDispatchable
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
 - IDMLDispatchable
---

# IDMLDispatchable interface


## -description

Implemented by objects that can be recorded into a command list for dispatch on the GPU, using [IDMLCommandRecorder::RecordDispatch](/windows/win32/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). The **IDMLDispatchable** interface inherits from [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable).

This interface is implemented by [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator) and [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer).

## -see-also

[IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable)
