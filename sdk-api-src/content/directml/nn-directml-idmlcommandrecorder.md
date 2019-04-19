---
UID: NN:directml.IDMLCommandRecorder
title: IDMLCommandRecorder
author: windows-sdk-content
description: Records dispatches of DirectML work into a Direct3D 12 command list.
old-location: direct3d12\idmlcommandrecorder.htm
tech.root: direct3d12
ms.assetid: 1DFE0E7A-FD83-47CD-9B1D-F70D8518FA29
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLCommandRecorder, IDMLCommandRecorder interface, IDMLCommandRecorder interface,described, direct3d12.idmlcommandrecorder, directml/IDMLCommandRecorder
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
 - IDMLCommandRecorder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLCommandRecorder interface


## -description






Records dispatches of DirectML work into a Direct3D 12 command list.

The command recorder is a stateless object whose purpose is to record commands into a Direct3D 12 command list. DirectML
    doesn't create command lists, command allocators, nor command queues; nor does it directly submit any work for
    execution on the GPU. Instead, your application manages its own command lists and queues, and it uses the
    <b>IDMLCommandRecorder</b> to record work into its existing command lists. You're then responsible for executing
    the command list on a queue of your choice.

This object is thread-safe.


## -inheritance

The <b>IDMLCommandRecorder</b> interface inherits from [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild). <b>IDMLCommandRecorder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMLCommandRecorder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch">RecordDispatch</a>
</td>
<td align="left" width="63%">

       Records execution of a dispatchable object (an operator initializer, or a compiled operator) onto a command
       list.

</td>
</tr>
</table> 


## -see-also




[IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild)
 

 

