---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
title: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT (d3d11.h)
description: Contains input data for a D3D11_AUTHENTICATED_QUERY_OUTPUT_ID query.
helpviewer_keywords: ["D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT","D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT","mf.d3d11_authenticated_query_output_id_input"]
old-location: mf\d3d11_authenticated_query_output_id_input.htm
tech.root: mf
ms.assetid: 2F4A6248-77DB-479B-B16C-81C3EE22937A
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT, D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT, mf.d3d11_authenticated_query_output_id_input
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
req.typenames: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
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
 - D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT
---

# D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT structure


## -description

Contains input data for a <b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID</b> query.

## -struct-fields

### -field Input

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input">D3D11_AUTHENTICATED_QUERY_INPUT</a> structure that contains the GUID for the query and other data.

### -field DeviceHandle

A handle to the device.

### -field CryptoSessionHandle

A handle to the cryptographic session.

### -field OutputIDIndex

The index of the output ID.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>