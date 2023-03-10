---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph).
helpviewer_keywords: ["DML_GRAPH_EDGE_DESC","DML_GRAPH_EDGE_DESC structure","direct3d12.dml_graph_edge_desc","directml/DML_GRAPH_EDGE_DESC"]
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
 - DML_GRAPH_EDGE_DESC
 - directml/DML_GRAPH_EDGE_DESC
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
 - DML_GRAPH_EDGE_DESC
---

## -description

A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph).

## -struct-fields

### -field Type
 
Type: **[DML_GRAPH_EDGE_TYPE](/windows/win32/api/directml/ne-directml-dml_graph_edge_type)**

The type of graph edge. See [DML_GRAPH_EDGE_TYPE](/windows/win32/api/directml/ne-directml-dml_graph_edge_type) for available types, and [DML_GRAPH_DESC](/windows/win32/api/directml/ns-directml-dml_graph_desc) for where to use each type.

### -field Desc
 
Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***

A pointer to the graph edge description. The type of the pointed-to struct must match the value specified in *Type*.

## Availability

This API was introduced in DirectML version `1.1.0`.

## -see-also

* [IDMLDevice1::CompileGraph method](/windows/desktop/api/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC structure](/windows/win32/api/directml/ns-directml-dml_graph_desc)
