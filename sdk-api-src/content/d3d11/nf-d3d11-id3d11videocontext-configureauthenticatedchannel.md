---
UID: NF:d3d11.ID3D11VideoContext.ConfigureAuthenticatedChannel
title: ID3D11VideoContext::ConfigureAuthenticatedChannel (d3d11.h)
description: Sends a configuration command to an authenticated channel.
helpviewer_keywords: ["ConfigureAuthenticatedChannel","ConfigureAuthenticatedChannel method [Media Foundation]","ConfigureAuthenticatedChannel method [Media Foundation]","ID3D11VideoContext interface","ID3D11VideoContext interface [Media Foundation]","ConfigureAuthenticatedChannel method","ID3D11VideoContext.ConfigureAuthenticatedChannel","ID3D11VideoContext::ConfigureAuthenticatedChannel","d3d11/ID3D11VideoContext::ConfigureAuthenticatedChannel","mf.id3d11videocontext_configureauthenticatedchannel"]
old-location: mf\id3d11videocontext_configureauthenticatedchannel.htm
tech.root: mf
ms.assetid: 6564EC13-A7B3-4A48-8776-4CD46BFF8E8F
ms.date: 12/05/2018
ms.keywords: ConfigureAuthenticatedChannel, ConfigureAuthenticatedChannel method [Media Foundation], ConfigureAuthenticatedChannel method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],ConfigureAuthenticatedChannel method, ID3D11VideoContext.ConfigureAuthenticatedChannel, ID3D11VideoContext::ConfigureAuthenticatedChannel, d3d11/ID3D11VideoContext::ConfigureAuthenticatedChannel, mf.id3d11videocontext_configureauthenticatedchannel
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012, None supported [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::ConfigureAuthenticatedChannel
 - d3d11/ID3D11VideoContext::ConfigureAuthenticatedChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.ConfigureAuthenticatedChannel
---

# ID3D11VideoContext::ConfigureAuthenticatedChannel


## -description

Sends a configuration command to an authenticated channel.

## -parameters

### -param pChannel [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel">ID3D11AuthenticatedChannel</a> interface.

### -param InputSize [in]

The size of the <i>pInput</i> array, in bytes.

### -param pInput [in]

A pointer to a byte array that contains input data for the command. This buffer always starts with a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure. The <b>ConfigureType</b> member of the structure specifies the command and defines the meaning of the rest of the buffer.

### -param pOutput [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output">D3D11_AUTHENTICATED_CONFIGURE_OUTPUT</a> structure that receives the response to the command.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>