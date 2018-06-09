---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT
title: D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT
author: windows-sdk-content
description: Contains input data for a D3D11_AUTHENTICATED_CONFIGURE_PROTECTION command.
old-location: mf\d3d11_authenticated_channel_configure_protection_input.htm
old-project: medfound
ms.assetid: 35BAED8D-B5AD-4ECA-B3ED-41871A2969FC
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT, D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT, mf.d3d11_authenticated_channel_configure_protection_input
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT structure


## -description


Contains input data for a <b>D3D11_AUTHENTICATED_CONFIGURE_PROTECTION</b> command.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/11FC071E-9B73-4960-B675-A43DDF75AA0B">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.




### -field Protections

A <a href="https://msdn.microsoft.com/037AB541-2E68-460C-8626-7F22C6C3E425">D3D11_AUTHENTICATED_PROTECTION_FLAGS</a> union that specifies the protection level.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

