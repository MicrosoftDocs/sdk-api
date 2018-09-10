---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
title: D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
author: windows-sdk-content
description: Contains the response from the ID3D11VideoContext::ConfigureAuthenticatedChannel method.
old-location: mf\d3d11_authenticated_configure_output.htm
tech.root: medfound
ms.assetid: 68DEC825-5D2E-4A78-B5DD-F7F697BB2980
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_OUTPUT, D3D11_AUTHENTICATED_CONFIGURE_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_OUTPUT, mf.d3d11_authenticated_configure_output
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
product: Windows
targetos: Windows
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
req.redist: 
---

# D3D11_AUTHENTICATED_CONFIGURE_OUTPUT structure


## -description


Contains the response from the <a href="https://msdn.microsoft.com/6564EC13-A7B3-4A48-8776-4CD46BFF8E8F">ID3D11VideoContext::ConfigureAuthenticatedChannel</a> method.


## -struct-fields




### -field omac

A <a href="https://msdn.microsoft.com/68AEC018-1DFE-4811-A511-176E82C2E9E2">D3D11_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.




### -field ConfigureType

A GUID that specifies the command. For a list of GUIDs, see <a href="https://msdn.microsoft.com/11FC071E-9B73-4960-B675-A43DDF75AA0B">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a>.


### -field hChannel

A handle to the authenticated channel.


### -field SequenceNumber

The command sequence number.


### -field ReturnCode

The result code for the command.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

