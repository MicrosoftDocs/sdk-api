---
UID: NE:d3d12.D3D12_INPUT_CLASSIFICATION
title: D3D12_INPUT_CLASSIFICATION (d3d12.h)

description: Identifies the type of data contained in an input slot.
old-location: direct3d12\d3d12_input_classification.htm
tech.root: direct3d12
ms.assetid: 09A14704-2E0B-4994-BED4-94F933A47317

ms.date: 12/05/2018
ms.keywords: D3D12_INPUT_CLASSIFICATION, D3D12_INPUT_CLASSIFICATION enumeration, D3D12_INPUT_CLASSIFICATION_PER_INSTANCE_DATA, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, d3d12/D3D12_INPUT_CLASSIFICATION, d3d12/D3D12_INPUT_CLASSIFICATION_PER_INSTANCE_DATA, d3d12/D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, direct3d12.d3d12_input_classification
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_INPUT_CLASSIFICATION"
dev_langs:
 - c++
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
 - D3D12_INPUT_CLASSIFICATION
targetos: Windows
req.typenames: D3D12_INPUT_CLASSIFICATION
req.redist: 
ms.custom: 19H1
---

# D3D12_INPUT_CLASSIFICATION enumeration


## -description


Identifies the type of data contained in an input slot.


## -enum-fields




### -field D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA

Input data is per-vertex data.


### -field D3D12_INPUT_CLASSIFICATION_PER_INSTANCE_DATA

Input data is per-instance data.


## -remarks



Specify one of these values in the member of a <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc">D3D12_INPUT_ELEMENT_DESC</a> structure to specify the type of data for the input element of a pipeline state object.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

