---
UID: NE:d3d11.D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE
title: D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE (d3d11.h)
description: Specifies the type of process that is identified in the D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT structure.
helpviewer_keywords: ["D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE","D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE enumeration [Media Foundation]","D3D11_PROCESSIDTYPE_DWM","D3D11_PROCESSIDTYPE_HANDLE","D3D11_PROCESSIDTYPE_UNKNOWN","d3d11/D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE","d3d11/D3D11_PROCESSIDTYPE_DWM","d3d11/D3D11_PROCESSIDTYPE_HANDLE","d3d11/D3D11_PROCESSIDTYPE_UNKNOWN","mf.d3d11_authenticated_process_identifier_type"]
old-location: mf\d3d11_authenticated_process_identifier_type.htm
tech.root: mf
ms.assetid: A8FFBBF1-7893-4D42-A8FB-1B7E56834603
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE, D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE enumeration [Media Foundation], D3D11_PROCESSIDTYPE_DWM, D3D11_PROCESSIDTYPE_HANDLE, D3D11_PROCESSIDTYPE_UNKNOWN, d3d11/D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE, d3d11/D3D11_PROCESSIDTYPE_DWM, d3d11/D3D11_PROCESSIDTYPE_HANDLE, d3d11/D3D11_PROCESSIDTYPE_UNKNOWN, mf.d3d11_authenticated_process_identifier_type
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
req.typenames: D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE
 - d3d11/D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE
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
 - D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE
---

# D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE enumeration


## -description

Specifies the type of process that is identified in the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_restricted_shared_resource_process_output">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT</a> structure.

## -enum-fields

### -field D3D11_PROCESSIDTYPE_UNKNOWN:0

Unknown process type.

### -field D3D11_PROCESSIDTYPE_DWM:1

Desktop Window Manager (DWM) process.

### -field D3D11_PROCESSIDTYPE_HANDLE:2

Handle to a process.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
