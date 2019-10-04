---
UID: NS:d3d12.D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT
title: D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT
author: windows-sdk-content
description: Contains a pointer to the head of a linked list of D3D12_AUTO_BREADCRUMB_NODE objects.
tech.root: direct3d12
ms.author: windowssdkdev
ms.date: 02/06/2019
ms.keywords: D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT, D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT structure, d3d12/D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT, direct3d12.d3d12_dred_auto_breadcrumbs_output
ms.topic: struct
f1_keywords: 
 - "d3d12/D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT"
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
 - d3d12.h
api_name:
 - D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT
targetos: Windows
req.typenames: D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT
req.redist: 
ms.custom: 19H1
---

# D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT structure

## -description

Contains a pointer to the head of a linked list of [D3D12_AUTO_BREADCRUMB_NODE](ns-d3d12-d3d12_auto_breadcrumb_node.md) objects. The list represents the auto-breadcrumb state prior to device removal.

## -struct-fields

### -field pHeadAutoBreadcrumbNode

A pointer to a constant [D3D12_AUTO_BREADCRUMB_NODE](ns-d3d12-d3d12_auto_breadcrumb_node.md) object representing the head of a linked list of auto-breadcrumb nodes, or `nullptr` if the list is empty.

## -see-also

* [Core structures](/windows/desktop/direct3d12/direct3d-12-structures)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)
