---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT (d3d11.h)
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_OUTPUT_ID query.
helpviewer_keywords: ["D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT","D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT","mf.d3d11_authenticated_query_output_id_output"]
old-location: mf\d3d11_authenticated_query_output_id_output.htm
tech.root: mf
ms.assetid: A7706E2B-B817-4D1C-B09D-D1803E0F8BFE
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT, D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT, mf.d3d11_authenticated_query_output_id_output
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
req.typenames: D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT
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
 - D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT
---

# D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT structure


## -description

Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID</b> query.

## -struct-fields

### -field Output

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.

### -field DeviceHandle

A handle to the device.

### -field CryptoSessionHandle

A handle to the cryptographic session.

### -field OutputIDIndex

The index of the output ID.

### -field OutputID

An output ID that is associated with the specified device and cryptographic session.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>