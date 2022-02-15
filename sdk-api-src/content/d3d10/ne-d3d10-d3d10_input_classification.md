---
UID: NE:d3d10.D3D10_INPUT_CLASSIFICATION
title: D3D10_INPUT_CLASSIFICATION (d3d10.h)
description: Type of data contained in an input slot.
helpviewer_keywords: ["324be834-c39b-26f0-18f5-c78924801214","D3D10_INPUT_CLASSIFICATION","D3D10_INPUT_CLASSIFICATION enumeration [Direct3D 10]","D3D10_INPUT_PER_INSTANCE_DATA","D3D10_INPUT_PER_VERTEX_DATA","d3d10/D3D10_INPUT_CLASSIFICATION","d3d10/D3D10_INPUT_PER_INSTANCE_DATA","d3d10/D3D10_INPUT_PER_VERTEX_DATA","direct3d10.d3d10_input_classification"]
old-location: direct3d10\d3d10_input_classification.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_input_classification.htm
ms.date: 12/05/2018
ms.keywords: 324be834-c39b-26f0-18f5-c78924801214, D3D10_INPUT_CLASSIFICATION, D3D10_INPUT_CLASSIFICATION enumeration [Direct3D 10], D3D10_INPUT_PER_INSTANCE_DATA, D3D10_INPUT_PER_VERTEX_DATA, d3d10/D3D10_INPUT_CLASSIFICATION, d3d10/D3D10_INPUT_PER_INSTANCE_DATA, d3d10/D3D10_INPUT_PER_VERTEX_DATA, direct3d10.d3d10_input_classification
req.header: d3d10.h
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
req.typenames: D3D10_INPUT_CLASSIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_INPUT_CLASSIFICATION
 - d3d10/D3D10_INPUT_CLASSIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_INPUT_CLASSIFICATION
---

# D3D10_INPUT_CLASSIFICATION enumeration


## -description

Type of data contained in an input slot.

## -enum-fields

### -field D3D10_INPUT_PER_VERTEX_DATA:0

Input data is per-vertex data.

### -field D3D10_INPUT_PER_INSTANCE_DATA:1

Input data is per-instance data.

## -remarks

Use these values to specify the type of data for a particular input element (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_input_element_desc">D3D10_INPUT_ELEMENT_DESC</a>) of an input-layout object.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
