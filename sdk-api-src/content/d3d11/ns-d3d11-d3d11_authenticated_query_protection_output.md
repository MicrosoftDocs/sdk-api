---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT (d3d11.h)
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_PROTECTION query.
helpviewer_keywords: ["D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT","D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT","mf.d3d11_authenticated_query_protection_output"]
old-location: mf\d3d11_authenticated_query_protection_output.htm
tech.root: mf
ms.assetid: F70D5AFC-06A6-408D-A951-1280FBBF8E89
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT, D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT, mf.d3d11_authenticated_query_protection_output
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
req.typenames: D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
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
 - D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT
---

# D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT structure


## -description

Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_PROTECTION</b> query.

## -struct-fields

### -field Output

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.

### -field ProtectionFlags

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_protection_flags">D3D11_AUTHENTICATED_PROTECTION_FLAGS</a> union that specifies the protection level.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>