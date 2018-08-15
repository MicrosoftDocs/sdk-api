---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.Configure
title: IDirect3DAuthenticatedChannel9::Configure
author: windows-sdk-content
description: Sends a configuration command to the authenticated channel.
old-location: mf\idirect3dauthenticatedchannel9_configure.htm
old-project: medfound
ms.assetid: 12d15872-4f35-4a6d-ae99-bc9fa69ffe06
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: Configure, Configure method [Media Foundation], Configure method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, IDirect3DAuthenticatedChannel9 interface [Media Foundation],Configure method, IDirect3DAuthenticatedChannel9.Configure, IDirect3DAuthenticatedChannel9::Configure, d3d9/IDirect3DAuthenticatedChannel9::Configure, mf.idirect3dauthenticatedchannel9_configure
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.h
api_name:
 - IDirect3DAuthenticatedChannel9.Configure
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

