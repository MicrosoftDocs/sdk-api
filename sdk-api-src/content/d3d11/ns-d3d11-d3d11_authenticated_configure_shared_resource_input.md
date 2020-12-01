---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
title: D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT (d3d11.h)
description: Contains input data for a D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE command.
helpviewer_keywords: ["D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT","D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT","mf.d3d11_authenticated_configure_shared_resource_input"]
old-location: mf\d3d11_authenticated_configure_shared_resource_input.htm
tech.root: mf
ms.assetid: 5AE1D03F-1853-45DA-96DC-BF1AACF6945F
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT, D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT, mf.d3d11_authenticated_configure_shared_resource_input
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
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
 - d3d11/D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
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
 - D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
---

# D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT structure


## -description

Contains input data for a <b>D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE</b> command.

## -struct-fields

### -field Parameters

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.

### -field ProcessType

A <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_authenticated_process_identifier_type">D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE</a> value that specifies the type of process.

To specify the Desktop Window Manager (DWM) process, set this member to <b>D3D11_PROCESSIDTYPE_DWM</b>. Otherwise, set this member to <b>D3D11_PROCESSIDTYPE_HANDLE</b> and set the <b>ProcessHandle</b> member to a valid handle.

### -field ProcessHandle

A process handle. If the <b>ProcessType</b> member equals <b>D3D11_PROCESSIDTYPE_HANDLE</b>, the <b>ProcessHandle</b> member specifies a handle to a process. Otherwise, the value is ignored.

### -field AllowAccess

If <b>TRUE</b>, the specified process has access to restricted shared resources.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>