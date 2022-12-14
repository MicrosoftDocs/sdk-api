---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/api/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph). This structure is used to define a connection from a graph input to an input of an internal node.
helpviewer_keywords: ["DML_INPUT_GRAPH_EDGE_DESC","DML_INPUT_GRAPH_EDGE_DESC structure","direct3d12.dml_input_graph_edge_desc","directml/DML_INPUT_GRAPH_EDGE_DESC"]
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
 - DML_INPUT_GRAPH_EDGE_DESC
 - directml/DML_INPUT_GRAPH_EDGE_DESC
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
 - DML_INPUT_GRAPH_EDGE_DESC
---

## -description

Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/api/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph). This structure is used to define a connection from a graph input to an input of an internal node.

## -struct-fields

### -field GraphInputIndex
 
Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The index of the graph input from which a connection to an internal node input is specified.

### -field ToNodeIndex
 
Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The index of the internal node onto which the connection from the graph input is specified.

### -field ToNodeInputIndex
 
Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The index of the input on the internal node where the connection is specified.

### -field Name

Type: \_Field\_z\_ \_Maybenull\_ **const char\***

An optional name for the graph connection. If provided, this might be used within certain error messages emitted by the DirectML debug layer.

## Availability

This API was introduced in DirectML version `1.1.0`.

## -see-also

* [IDMLDevice1::CompileGraph method](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC structure](/windows/desktop/api/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_EDGE_DESC structure](/windows/desktop/api/directml/ns-directml-dml_graph_edge_desc)
