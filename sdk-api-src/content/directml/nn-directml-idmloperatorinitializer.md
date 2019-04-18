---
UID: NN:directml.IDMLOperatorInitializer
title: IDMLOperatorInitializer
author: windows-sdk-content
description: Represents a specialized object whose purpose is to initialize compiled operators. To create an instance of this object, call IDMLDevice::CreateOperatorInitializer.
old-location: direct3d12\idmloperatorinitializer.htm
tech.root: direct3d12
ms.assetid: 86DB9277-ECA6-4D0C-82A5-88D7E9674AC7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLOperatorInitializer, IDMLOperatorInitializer interface, IDMLOperatorInitializer interface,described, direct3d12.idmloperatorinitializer, directml/IDMLOperatorInitializer
ms.topic: interface
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
 - IDMLOperatorInitializer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLOperatorInitializer interface


## -description






Represents a specialized object whose purpose is to initialize compiled operators. To create an instance
    of this object, call [IDMLDevice::CreateOperatorInitializer](/windows/desktop/api/directml/nf-directml-idmldevice-createoperatorinitializer).

An operator initializer is associated with one or more compiled operators, which are the targets for initialization.
    You can record operator initialization onto a command list using [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).
    When the initialization completes execution on the GPU, all of the target operators enter the
    initialized state. You must initialize all operators exactly once before they can be executed.


## -inheritance

The <b>IDMLOperatorInitializer</b> interface inherits from [IDMLDispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable). <b>IDMLOperatorInitializer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMLOperatorInitializer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the initializer to handle initialization of a new set of operators.

</td>
</tr>
</table> 


## -remarks



Operator initializers are reusable: once an instance has been used to initialize a set of operators, you can reset it with a different set of compiled operators as targets.

When executing an initializer, the expected bindings are as follows:

- Inputs should be one buffer array binding for each target operator, in the order that you originally specified the operators when creating or resetting the initializer. Each buffer array binding itself should have a size equal to the inputs of its respective operator. Alternatively, you may specify NONE for a binding to bind no inputs for initialization of that target operator.
- Outputs should be the persistent resources for each target operator, in the order that you originally specified the operators when creating or resetting the initializer.
- As with any dispatchable object (an operator initializer, or a compiled operator), the initializer may require a temporary resource. Call [IDMLDispatchable::GetBindingProperties](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) to determine the require size of the temporary resource.
- Operator initializers don't ever require persistent resources. Therefore, calling [IDMLDispatchable::GetBindingProperties](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) on an operator initializer always returns a <b>PersistentResourceSize</b> of 0.

The operator initializer itself doesn't need to be initialized—GPU initialization only applies to compiled operators.

## -see-also

<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>

[IDMLDispatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable)
