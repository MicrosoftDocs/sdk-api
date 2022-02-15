---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Defines constants that specify a type of graph edge. See [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) for the usage of this enumeration.
helpviewer_keywords: ["DML_GRAPH_EDGE_TYPE","DML_GRAPH_EDGE_TYPE structure","direct3d12.dml_graph_edge_type","directml/DML_GRAPH_EDGE_TYPE"]
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - DML_GRAPH_EDGE_TYPE
 - directml/DML_GRAPH_EDGE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_GRAPH_EDGE_TYPE
---

## -description

Defines constants that specify a type of graph edge. See [DML_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc) for the usage of this enumeration.

## -enum-fields

### -field DML_GRAPH_EDGE_TYPE_INVALID

Specifies an unknown graph edge type, and is never valid. Using this value results in an error.

### -field DML_GRAPH_EDGE_TYPE_INPUT

Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_input_graph_edge_desc) structure.

### -field DML_GRAPH_EDGE_TYPE_OUTPUT

Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_output_graph_edge_desc) structure.

### -field DML_GRAPH_EDGE_TYPE_INTERMEDIATE

Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](/windows/win32/api/directml/ns-directml-dml_intermediate_graph_edge_desc) structure.

## Availability

This API was introduced in DirectML version `1.1.0`.

## -see-also

* [IDMLDevice1::CompileGraph method](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC structure](/windows/win32/api/directml/ns-directml-dml_graph_desc)     
* [DML_GRAPH_EDGE_DESC structure](/windows/win32/api/directml/ns-directml-dml_graph_edge_desc)
* [DML_INPUT_GRAPH_EDGE_DESC structure](/windows/win32/api/directml/ns-directml-dml_input_graph_edge_desc)
* [DML_OUTPUT_GRAPH_EDGE_DESC structure](/windows/win32/api/directml/ns-directml-dml_output_graph_edge_desc)
* [DML_INTERMEDIATE_GRAPH_EDGE_DESC structure](/windows/win32/api/directml/ns-directml-dml_intermediate_graph_edge_desc)
