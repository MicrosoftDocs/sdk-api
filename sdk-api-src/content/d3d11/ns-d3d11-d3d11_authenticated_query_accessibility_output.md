---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_ACESSIBILITY_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT (d3d11.h)
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES query.
helpviewer_keywords: ["D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT","D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT","mf.d3d11_authenticated_query_accessibility_output"]
old-location: mf\d3d11_authenticated_query_accessibility_output.htm
tech.root: mf
ms.assetid: 1E2EBE2C-3749-47B5-B7A8-3EAE371981DB
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT, D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT, mf.d3d11_authenticated_query_accessibility_output
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_QUERY_ACESSIBILITY_OUTPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_ACESSIBILITY_OUTPUT
 - D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT
---

# D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT structure


## -description

Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES</b> query.

## -struct-fields

### -field Output

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.

### -field BusType

A bitwise <b>OR</b> of flags from the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bus_type">D3D11_BUS_TYPE</a> enumeration.

### -field AccessibleInContiguousBlocks

If <b>TRUE</b>, contiguous blocks of video memory may be accessible to the CPU or the bus.

### -field AccessibleInNonContiguousBlocks

If <b>TRUE</b>, non-contiguous blocks of video memory may be accessible to the CPU or the bus.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>