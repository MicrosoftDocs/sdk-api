---
UID: NN:d3d12.ID3D12MetaCommand
title: ID3D12MetaCommand (d3d12.h)
description: Represents a meta command. A meta command is a Direct3D 12 object representing an algorithm that is accelerated by independent hardware vendors (IHVs). It's an opaque reference to a command generator that is implemented by the driver.
helpviewer_keywords: ["ID3D12MetaCommand","ID3D12MetaCommand interface","ID3D12MetaCommand interface","described","d3d12/ID3D12MetaCommand","direct3d12.id3d12metacommand"]
old-location: direct3d12\id3d12metacommand.htm
tech.root: direct3d12
ms.assetid: 976A7F78-1801-47DD-9350-21F530B4D145
ms.date: 12/05/2018
ms.keywords: ID3D12MetaCommand, ID3D12MetaCommand interface, ID3D12MetaCommand interface,described, d3d12/ID3D12MetaCommand, direct3d12.id3d12metacommand
req.header: d3d12.h
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
 - ID3D12MetaCommand
 - d3d12/ID3D12MetaCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.h
api_name:
 - ID3D12MetaCommand
---

# ID3D12MetaCommand interface


## -description

Represents a meta command. A meta command is a Direct3D 12 object representing an algorithm that is accelerated by independent hardware vendors (IHVs). It's an opaque reference to a command generator that is implemented by the driver.

The lifetime of a meta command is tied to the lifetime of the command list that references it. So, you should only free a meta command if no command list referencing it is currently executing on the GPU.

A meta command can encapsulate a set of pipeline state objects (PSOs), bindings, intermediate resource states, and Draw/Dispatch calls. You can think of the signature of a meta command as being similar to a C-style function, with multiple in/out parameters, and no return value.

## -inheritance

The <b>ID3D12MetaCommand</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>. <b>ID3D12MetaCommand</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>
