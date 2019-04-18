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






Implemented by objects that can be recorded into a command list for dispatch on the GPU, using
    [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

This interface is implemented by [IDMLCompiledOperator](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) and [IDMLOperatorInitializer](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer).


## -inheritance

The <b>IDMLDispatchable</b> interface inherits from [IDMLPageable](/windows/desktop/api/directml/nn-directml-idmlpageable). <b>IDMLDispatchable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMLDispatchable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties">GetBindingProperties</a>
</td>
<td align="left" width="63%">

       Retrieves the binding properties for a dispatchable object (an operator initializer, or a compiled operator). The binding properties
       value contains the required size of the binding table in descriptors, as well as the required size in bytes of the
       temporary and persistent resources required to execute this object.

</td>
</tr>
</table> 


## -see-also




[IDMLPageable](/windows/desktop/api/directml/nn-directml-idmlpageable)
 

 

