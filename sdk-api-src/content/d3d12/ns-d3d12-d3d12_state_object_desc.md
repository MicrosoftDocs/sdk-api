---
UID: NS:d3d12.D3D12_STATE_OBJECT_DESC
title: D3D12_STATE_OBJECT_DESC (d3d12.h)
author: windows-sdk-content
description: Description of a state object. Pass this structure into ID3D12Device::CreateStateObject.
old-location: direct3d12\d3d12_state_object_desc.htm
tech.root: direct3d12
ms.assetid: 034B3573-4351-4BB4-AB5C-A15DB679CD00
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_STATE_OBJECT_DESC, D3D12_STATE_OBJECT_DESC structure, PD3D12_STATE_OBJECT_DESC, PD3D12_STATE_OBJECT_DESC structure pointer, d3d12/D3D12_STATE_OBJECT_DESC, d3d12/PD3D12_STATE_OBJECT_DESC, direct3d12.d3d12_state_object_desc
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_STATE_OBJECT_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_STATE_OBJECT_DESC
req.redist: 
---

# D3D12_STATE_OBJECT_DESC structure


## -description


Description of a state object. Pass this structure into <a href="nf-d3d12-id3d12device5-createstateobject">ID3D12Device5::CreateStateObject</a>.


## -struct-fields




### -field Type

The type of the state object.


### -field NumSubobjects

Size of the <i>pSubobjects</i> array.


### -field pSubobjects

An array of subobject definitions.

