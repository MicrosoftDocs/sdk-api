---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

