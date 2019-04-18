---
UID: NN:directml.IDMLDevice
title: IDMLDevice
author: windows-sdk-content
description: Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.
old-location: direct3d12\idmldevice.htm
tech.root: direct3d12
ms.assetid: C6E13DEF-1FE1-416E-9917-ECE20FBCA401
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLDevice, IDMLDevice interface, IDMLDevice interface,described, direct3d12.idmldevice, directml/IDMLDevice
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
 - IDMLDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDevice interface


## -description






Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other
    objects.

A DirectML device is always associated with exactly one underlying Direct3D 12 device. All objects created by the
    DirectML device maintain a strong reference to their parent device. Unlike the Direct3D 12 device, the DML device is not
    a singleton. Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device. However, this
    isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple
    DML devices over the same Direct3D 12 device.

This object is thread-safe.


## -inheritance

The <b>IDMLDevice</b> interface inherits from [IDMLObject](/windows/desktop/api/directml/nn-directml-idmlobject). <b>IDMLDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMLDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-checkfeaturesupport">CheckFeatureSupport</a>
</td>
<td align="left" width="63%">
Gets information about the optional features and capabilities that are supported by the DirectML device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-compileoperator">CompileOperator</a>
</td>
<td align="left" width="63%">
Compiles an operator into an object that can be dispatched to the GPU.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable">CreateBindingTable</a>
</td>
<td align="left" width="63%">
Creates a binding table, which is an object that can be used to bind resources (such as tensors) to the pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-createcommandrecorder">CreateCommandRecorder</a>
</td>
<td align="left" width="63%">
Creates a DirectML command recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-createoperator">CreateOperator</a>
</td>
<td align="left" width="63%">
Creates a DirectML operator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-createoperatorinitializer">CreateOperatorInitializer</a>
</td>
<td align="left" width="63%">
Creates an object that can be used to initialize compiled operators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-evict">Evict</a>
</td>
<td align="left" width="63%">
Evicts one or more pageable objects from GPU memory. Also see [IDMLDevice::MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason">GetDeviceRemovedReason</a>
</td>
<td align="left" width="63%">
Retrieves the reason that the DirectML device was removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-getparentdevice">GetParentDevice</a>
</td>
<td align="left" width="63%">
Retrieves the Direct3D 12 device that was used to create this DirectML device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
**LoadCompiledOperator**
</td>
<td align="left" width="63%">
Loads a previously-compiled operator from the given pipeline library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldevice-makeresident">MakeResident</a>
</td>
<td align="left" width="63%">
Causes one or more pageable objects to become resident in GPU memory. Also see [IDMLDevice::Evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict).

</td>
</tr>
</table> 


## -see-also




[IDMLObject](/windows/desktop/api/directml/nn-directml-idmlobject)
 

 

