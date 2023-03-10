---
UID: NN:directml.IDMLCommandRecorder
title: IDMLCommandRecorder
description: Records dispatches of DirectML work into a Direct3D 12 command list.
helpviewer_keywords: ["IDMLCommandRecorder","IDMLCommandRecorder interface","IDMLCommandRecorder interface","described","direct3d12.idmlcommandrecorder","directml/IDMLCommandRecorder"]
old-location: direct3d12\idmlcommandrecorder.htm
tech.root: directml
ms.assetid: 1DFE0E7A-FD83-47CD-9B1D-F70D8518FA29
ms.date: 12/5/2018
ms.keywords: IDMLCommandRecorder, IDMLCommandRecorder interface, IDMLCommandRecorder interface,described, direct3d12.idmlcommandrecorder, directml/IDMLCommandRecorder
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
 - IDMLCommandRecorder
 - directml/IDMLCommandRecorder
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
 - IDMLCommandRecorder
---

# IDMLCommandRecorder interface


## -description

Records dispatches of DirectML work into a Direct3D 12 command list. The **IDMLCommandRecorder** interface inherits from [IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild).

The command recorder is a stateless object whose purpose is to record commands into a Direct3D 12 command list. DirectML
    doesn't create command lists, command allocators, nor command queues; nor does it directly submit any work for
    execution on the GPU. Instead, your application manages its own command lists and queues, and it uses the
    <b>IDMLCommandRecorder</b> to record work into its existing command lists. You're then responsible for executing
    the command list on a queue of your choice.

This object is thread-safe.

## -see-also

[IDMLDeviceChild](/windows/win32/api/directml/nn-directml-idmldevicechild)
