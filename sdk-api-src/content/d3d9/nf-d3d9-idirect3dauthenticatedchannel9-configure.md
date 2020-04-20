---
UID: NF:d3d9.IDirect3DAuthenticatedChannel9.Configure
title: IDirect3DAuthenticatedChannel9::Configure (d3d9.h)
description: Sends a configuration command to the authenticated channel.helpviewer_keywords: ["Configure","Configure method [Media Foundation]","Configure method [Media Foundation]","IDirect3DAuthenticatedChannel9 interface","IDirect3DAuthenticatedChannel9 interface [Media Foundation]","Configure method","IDirect3DAuthenticatedChannel9.Configure","IDirect3DAuthenticatedChannel9::Configure","d3d9/IDirect3DAuthenticatedChannel9::Configure","mf.idirect3dauthenticatedchannel9_configure"]
old-location: mf\idirect3dauthenticatedchannel9_configure.htm
tech.root: medfound
ms.assetid: 12d15872-4f35-4a6d-ae99-bc9fa69ffe06
ms.date: 12/05/2018
ms.keywords: Configure, Configure method [Media Foundation], Configure method [Media Foundation],IDirect3DAuthenticatedChannel9 interface, IDirect3DAuthenticatedChannel9 interface [Media Foundation],Configure method, IDirect3DAuthenticatedChannel9.Configure, IDirect3DAuthenticatedChannel9::Configure, d3d9/IDirect3DAuthenticatedChannel9::Configure, mf.idirect3dauthenticatedchannel9_configure
f1_keywords:
- d3d9/IDirect3DAuthenticatedChannel9.Configure
dev_langs:
- c++
req.header: d3d9.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d9.h
api_name:
- IDirect3DAuthenticatedChannel9.Configure
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DAuthenticatedChannel9::Configure


## -description


Sends a configuration command to the authenticated channel.


## -parameters




### -param InputSize

The size of the <i>pInput</i> array, in bytes.


### -param pInput

A pointer to a byte array that contains input data for the command. This buffer always starts with a <a href="https://docs.microsoft.com/windows/desktop/medfound/d3dauthenticatedchannel-configure-input">D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT</a> structure. The <b>ConfigureType</b> member of the structure specifies the command and defines the meaning of the rest of the buffer.


### -param pOutput

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/medfound/d3dauthenticatedchannel-configure-output">D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT</a> structure that receives the response to the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of commands, see <a href="https://docs.microsoft.com/windows/desktop/medfound/content-protection-commands">Content Protection Commands</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/content-protection-commands">Content Protection Commands</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/gpu-based-content-protection">GPU-Based Content Protection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9">IDirect3DAuthenticatedChannel9</a>
 

 

