---
UID: NE:d2d1_3.D2D1_PATCH_EDGE_MODE
title: D2D1_PATCH_EDGE_MODE (d2d1_3.h)
description: Specifies how to render gradient mesh edges.
helpviewer_keywords: ["D2D1_PATCH_EDGE_MODE","D2D1_PATCH_EDGE_MODE enumeration [Direct2D]","D2D1_PATCH_EDGE_MODE_ALIASED","D2D1_PATCH_EDGE_MODE_ALIASED_INFLATED","D2D1_PATCH_EDGE_MODE_ANTIALIASED","d2d1_3/D2D1_PATCH_EDGE_MODE","d2d1_3/D2D1_PATCH_EDGE_MODE_ALIASED","d2d1_3/D2D1_PATCH_EDGE_MODE_ALIASED_INFLATED","d2d1_3/D2D1_PATCH_EDGE_MODE_ANTIALIASED","direct2d.d2d1_patch_edge_mode"]
old-location: direct2d\d2d1_patch_edge_mode.htm
tech.root: Direct2D
ms.assetid: 5AE38632-B068-4A14-9DAB-67FD58E3894B
ms.date: 12/05/2018
ms.keywords: D2D1_PATCH_EDGE_MODE, D2D1_PATCH_EDGE_MODE enumeration [Direct2D], D2D1_PATCH_EDGE_MODE_ALIASED, D2D1_PATCH_EDGE_MODE_ALIASED_INFLATED, D2D1_PATCH_EDGE_MODE_ANTIALIASED, d2d1_3/D2D1_PATCH_EDGE_MODE, d2d1_3/D2D1_PATCH_EDGE_MODE_ALIASED, d2d1_3/D2D1_PATCH_EDGE_MODE_ALIASED_INFLATED, d2d1_3/D2D1_PATCH_EDGE_MODE_ANTIALIASED, direct2d.d2d1_patch_edge_mode
req.header: d2d1_3.h
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
req.typenames: D2D1_PATCH_EDGE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_PATCH_EDGE_MODE
 - d2d1_3/D2D1_PATCH_EDGE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_PATCH_EDGE_MODE
---

# D2D1_PATCH_EDGE_MODE enumeration


## -description

Specifies how to render gradient mesh edges.

## -enum-fields

### -field D2D1_PATCH_EDGE_MODE_ALIASED:0

Render this patch edge aliased. Use this value for the internal edges of your gradient mesh.

### -field D2D1_PATCH_EDGE_MODE_ANTIALIASED:1

Render this patch edge antialiased. Use this value for the external (boundary) edges of your mesh.

### -field D2D1_PATCH_EDGE_MODE_ALIASED_INFLATED:2

Render this patch edge aliased and also slightly inflated. Use this for the internal edges of your gradient mesh when there could be t-junctions among patches. 
          Inflating the internal edges mitigates seams that can appear along those junctions.

### -field D2D1_PATCH_EDGE_MODE_FORCE_DWORD:0xffffffff

