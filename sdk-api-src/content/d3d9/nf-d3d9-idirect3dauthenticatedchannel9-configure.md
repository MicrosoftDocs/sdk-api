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

# IDirect3DAuthenticatedChannel9::Configure


## -description


Sends a configuration command to the authenticated channel.


## -parameters




### -param InputSize

The size of the <i>pInput</i> array, in bytes.


### -param pInput

A pointer to a byte array that contains input data for the command. This buffer always starts with a <a href="https://msdn.microsoft.com/7646100e-f768-4935-9e71-1d9db0d69c52">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure. The <b>ConfigureType</b> member of the structure specifies the command and defines the meaning of the rest of the buffer.


### -param pOutput

A pointer to a <a href="https://msdn.microsoft.com/6f33d3f7-a883-4aca-a058-b656d745f2b1">D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT</a> structure that receives the response to the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of commands, see <a href="https://msdn.microsoft.com/86be7dcf-7b7b-455a-a6ac-8a82b34fdafc">Content Protection Commands</a>. 




## -see-also




<a href="https://msdn.microsoft.com/86be7dcf-7b7b-455a-a6ac-8a82b34fdafc">Content Protection Commands</a>



<a href="https://msdn.microsoft.com/FD0625BB-484A-43E6-8931-DB635D4F017F">GPU-Based Content Protection</a>



<a href="https://msdn.microsoft.com/dd969956-a140-44ed-9917-5a0a09a432fa">IDirect3DAuthenticatedChannel9</a>
 

 

