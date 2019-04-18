---
UID: NN:directml.IDMLDebugDevice
title: IDMLDebugDevice
author: windows-sdk-content
description: Controls the DirectML debug layers.
old-location: direct3d12\idmldebugdevice.htm
tech.root: direct3d12
ms.assetid: 6602B70E-19EA-4C3D-B01C-16EC4830AB7F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLDebugDevice, IDMLDebugDevice interface, IDMLDebugDevice interface,described, direct3d12.idmldebugdevice, directml/IDMLDebugDevice
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
 - IDMLDebugDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDebugDevice interface


## -description






Controls the DirectML debug layers.

 This interface may be retrieved from the [IDMLDevice](/windows/desktop/api/directml/nn-directml-idmldevice) via QueryInterface. This
    interface is only available if the DirectML device was created with the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/desktop/api/directml/ne-directml-dml_create_device_flags) flag. DirectML
    sends messages to the <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a> associated with the <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a> passed in at [DMLCreateDevice](/windows/desktop/api/directml/nf-directml-dmlcreatedevice); the Direct3D 12
    info queue can be retrieved via QueryInterface on the <b>ID3D12Device</b>

This object is thread-safe.


## -inheritance

The <b>IDMLDebugDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDMLDebugDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMLDebugDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmldebugdevice-setmutedebugoutput">SetMuteDebugOutput</a>
</td>
<td align="left" width="63%">
Determine whether to mute DirectML from sending messages to the <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>.

</td>
</tr>
</table> 

