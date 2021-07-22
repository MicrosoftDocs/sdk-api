---
UID: NF:d3d11.ID3D11VideoContext.NegotiateAuthenticatedChannelKeyExchange
title: ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange (d3d11.h)
description: Establishes a session key for an authenticated channel.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","NegotiateAuthenticatedChannelKeyExchange method","ID3D11VideoContext.NegotiateAuthenticatedChannelKeyExchange","ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange","NegotiateAuthenticatedChannelKeyExchange","NegotiateAuthenticatedChannelKeyExchange method [Media Foundation]","NegotiateAuthenticatedChannelKeyExchange method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange","mf.id3d11videocontext_negotiateauthenticatedchannelkeyexchange"]
old-location: mf\id3d11videocontext_negotiateauthenticatedchannelkeyexchange.htm
tech.root: mf
ms.assetid: FF546AE5-D062-41A9-B143-8B25466BF6E3
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],NegotiateAuthenticatedChannelKeyExchange method, ID3D11VideoContext.NegotiateAuthenticatedChannelKeyExchange, ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange, NegotiateAuthenticatedChannelKeyExchange, NegotiateAuthenticatedChannelKeyExchange method [Media Foundation], NegotiateAuthenticatedChannelKeyExchange method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange, mf.id3d11videocontext_negotiateauthenticatedchannelkeyexchange
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange
 - d3d11/ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange
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
 - ID3D11VideoContext.NegotiateAuthenticatedChannelKeyExchange
---

# ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange


## -description

Establishes a session key for an authenticated channel.

## -parameters

### -param pChannel [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel">ID3D11AuthenticatedChannel</a> interface.  This method will fail if the channel type is    <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_authenticated_channel_type">D3D11_AUTHENTICATED_CHANNEL_D3D11</a>, because the Direct3D11 channel does not support authentication.

### -param DataSize [in]

The size of the data in the <i>pData</i> array, in bytes.

### -param pData [in, out]

A pointer to a byte array that contains the encrypted session key. The buffer must contain 256 bytes of data, encrypted using RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method will fail if the channel type is    <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_authenticated_channel_type">D3D11_AUTHENTICATED_CHANNEL_D3D11</a>, because the Direct3D11 channel does not support authentication.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>