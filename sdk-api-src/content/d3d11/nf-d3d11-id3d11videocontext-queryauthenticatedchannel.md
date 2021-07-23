---
UID: NF:d3d11.ID3D11VideoContext.QueryAuthenticatedChannel
title: ID3D11VideoContext::QueryAuthenticatedChannel (d3d11.h)
description: Sends a query to an authenticated channel.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","QueryAuthenticatedChannel method","ID3D11VideoContext.QueryAuthenticatedChannel","ID3D11VideoContext::QueryAuthenticatedChannel","QueryAuthenticatedChannel","QueryAuthenticatedChannel method [Media Foundation]","QueryAuthenticatedChannel method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::QueryAuthenticatedChannel","mf.id3d11videocontext_queryauthenticatedchannel"]
old-location: mf\id3d11videocontext_queryauthenticatedchannel.htm
tech.root: mf
ms.assetid: 4E059358-E1FD-4EDB-B1D4-982802385232
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],QueryAuthenticatedChannel method, ID3D11VideoContext.QueryAuthenticatedChannel, ID3D11VideoContext::QueryAuthenticatedChannel, QueryAuthenticatedChannel, QueryAuthenticatedChannel method [Media Foundation], QueryAuthenticatedChannel method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::QueryAuthenticatedChannel, mf.id3d11videocontext_queryauthenticatedchannel
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
 - ID3D11VideoContext::QueryAuthenticatedChannel
 - d3d11/ID3D11VideoContext::QueryAuthenticatedChannel
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
 - ID3D11VideoContext.QueryAuthenticatedChannel
---

# ID3D11VideoContext::QueryAuthenticatedChannel


## -description

Sends a query to an authenticated channel.

## -parameters

### -param pChannel [in]

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel">ID3D11AuthenticatedChannel</a> interface.

### -param InputSize [in]

The size of the <i>pInput</i> array, in bytes.

### -param pInput [in]

A pointer to a byte array that contains input data for the query. This array always starts with a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input">D3D11_AUTHENTICATED_QUERY_INPUT</a> structure. The <b>QueryType</b> member of the structure specifies the query and defines the meaning of the rest of the array.

### -param OutputSize [in]

The size of the <i>pOutput</i> array, in bytes.

### -param pOutput [out]

A pointer to a byte array that receives the result of the query. This array always starts with a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output">D3D11_AUTHENTICATED_QUERY_OUTPUT</a> structure. The meaning of the rest of the array depends on the query.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>