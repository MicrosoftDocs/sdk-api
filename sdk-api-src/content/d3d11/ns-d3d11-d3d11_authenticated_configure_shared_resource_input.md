---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
title: D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
author: windows-sdk-content
description: Contains input data for a D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE command.
old-location: mf\d3d11_authenticated_configure_shared_resource_input.htm
old-project: medfound
ms.assetid: 5AE1D03F-1853-45DA-96DC-BF1AACF6945F
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT, D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT, mf.d3d11_authenticated_configure_shared_resource_input
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT structure


## -description


Contains input data for a <b>D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE</b> command.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/11FC071E-9B73-4960-B675-A43DDF75AA0B">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.




### -field ProcessType

A <a href="https://msdn.microsoft.com/A8FFBBF1-7893-4D42-A8FB-1B7E56834603">D3D11_AUTHENTICATED_PROCESS_IDENTIFIER_TYPE</a> value that specifies the type of process.

To specify the Desktop Window Manager (DWM) process, set this member to <b>D3D11_PROCESSIDTYPE_DWM</b>. Otherwise, set this member to <b>D3D11_PROCESSIDTYPE_HANDLE</b> and set the <b>ProcessHandle</b> member to a valid handle.


### -field ProcessHandle

A process handle. If the <b>ProcessType</b> member equals <b>D3D11_PROCESSIDTYPE_HANDLE</b>, the <b>ProcessHandle</b> member specifies a handle to a process. Otherwise, the value is ignored.


### -field AllowAccess

If <b>TRUE</b>, the specified process has access to restricted shared resources.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

