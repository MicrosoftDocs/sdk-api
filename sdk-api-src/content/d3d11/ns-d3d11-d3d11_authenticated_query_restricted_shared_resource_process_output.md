---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT
title: D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT (d3d11.h)
description: Contains the response to a D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS query.
helpviewer_keywords: ["D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT","D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT","mf.d3d11_authenticated_query_restricted_shared_resource_process_output"]
old-location: mf\d3d11_authenticated_query_restricted_shared_resource_process_output.htm
tech.root: mf
ms.assetid: 0668B546-6825-4AD9-85CF-CA238028B2E3
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT, D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT, mf.d3d11_authenticated_query_restricted_shared_resource_process_output
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
req.typenames: D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT
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
 - D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT
---

## -description

Contains the response to a <b>D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS</b> query.

## -struct-fields

### -field Output

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure that contains a Message Authentication Code (MAC) and other data.

### -field ProcessIndex

The index of the process in the list of processes.

### -field ProcessIdentifier

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_authenticated_process_identifier_type">D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE</a> value that specifies the type of process.

### -field ProcessHandle

A process handle. If the <b>ProcessIdentifier</b> member equals <b>D3D11_PROCESSIDTYPE_HANDLE</b>, the <b>ProcessHandle</b> member contains a valid handle to a process. Otherwise, this member is ignored.

## -remarks

The Desktop Window Manager (DWM) process is identified by setting <b>ProcessIdentifier</b> equal to <b>D3D11_PROCESSIDTYPE_DWM</b>. Other processes are identified by setting the process handle in <b>ProcessHandle</b> and setting <b>ProcessIdentifier</b> equal to <b>D3D11_PROCESSIDTYPE_HANDLE</b>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>