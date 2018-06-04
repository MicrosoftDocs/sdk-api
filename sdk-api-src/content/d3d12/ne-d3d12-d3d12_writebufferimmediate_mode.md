---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_WRITEBUFFERIMMEDIATE_MODE enumeration


## -description


Specifies the mode used by a <b>WriteBufferImmediate</b> operation.


## -enum-fields




### -field D3D12_WRITEBUFFERIMMEDIATE_MODE_DEFAULT

The write operation behaves the same as normal copy-write operations.


### -field D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN

The write operation is guaranteed to occur after all preceding commands in the command stream have started, including previous <b>WriteBufferImmediate</b> operations.


### -field D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT

The write operation is deferred until all previous commands in the command stream have completed through the GPU pipeline, including previous <b>WriteBufferImmediate</b> operations. Write operations that specify <b>D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_OUT</b> don't block subsequent operations from starting. If there are no previous operations in the command stream, then the write operation behaves as if <b>D3D12_WRITEBUFFERIMMEDIATE_MODE_MARKER_IN</b> was specified.


## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/6A1BF079-CAE7-45E9-A95F-E19ACD380143">ID3D12GraphicsCommandList::WriteBufferImmediate</a>
 

 

