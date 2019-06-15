---
UID: NN:directml.IDMLDispatchable
title: IDMLDispatchable
author: windows-sdk-content
description: Implemented by objects that can be recorded into a command list for dispatch on the GPU, using IDMLCommandRecorder::RecordDispatch.
old-location: direct3d12\idmldispatchable.htm
tech.root: direct3d12
ms.assetid: 4CE57EB6-0738-4A5B-84FE-9761363F304B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLDispatchable, IDMLDispatchable interface, IDMLDispatchable interface,described, direct3d12.idmldispatchable, directml/IDMLDispatchable
ms.topic: interface
f1_keywords: ["directml/IDMLDispatchable"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLDispatchable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDispatchable interface

## -description

Implemented by objects that can be recorded into a command list for dispatch on the GPU, using [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).The **IDMLDispatchable** interface inherits from [IDMLPageable](/windows/desktop/api/directml/nn-directml-idmlpageable).

This interface is implemented by [IDMLCompiledOperator](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) and [IDMLOperatorInitializer](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer).

## -see-also
[IDMLPageable](/windows/desktop/api/directml/nn-directml-idmlpageable)
