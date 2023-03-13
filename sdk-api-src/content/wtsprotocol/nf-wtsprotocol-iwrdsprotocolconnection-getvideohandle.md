---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetVideoHandle
title: IWRdsProtocolConnection::GetVideoHandle (wtsprotocol.h)
description: Obtains the handle of the video device for the protocol.
helpviewer_keywords: ["GetVideoHandle","GetVideoHandle method [Remote Desktop Services]","GetVideoHandle method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetVideoHandle method","IWRdsProtocolConnection.GetVideoHandle","IWRdsProtocolConnection::GetVideoHandle","termserv.iwrdsprotocolconnection_getvideohandle","wtsprotocol/IWRdsProtocolConnection::GetVideoHandle"]
old-location: termserv\iwrdsprotocolconnection_getvideohandle.htm
tech.root: TermServ
ms.assetid: 069ee899-ae3a-4043-92b5-e193dbfe4f54
ms.date: 12/05/2018
ms.keywords: GetVideoHandle, GetVideoHandle method [Remote Desktop Services], GetVideoHandle method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetVideoHandle method, IWRdsProtocolConnection.GetVideoHandle, IWRdsProtocolConnection::GetVideoHandle, termserv.iwrdsprotocolconnection_getvideohandle, wtsprotocol/IWRdsProtocolConnection::GetVideoHandle
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
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
 - IWRdsProtocolConnection::GetVideoHandle
 - wtsprotocol/IWRdsProtocolConnection::GetVideoHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.GetVideoHandle
---

# IWRdsProtocolConnection::GetVideoHandle


## -description

Obtains the handle of the video device for the protocol.

## -parameters

### -param pVideoHandle [out]

A pointer to a handle that receives the handle of the video device.

If the protocol object is using the <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection.md">IWRdsRemoteFXGraphicsConnection</a>  interface, this method should set the contents of <i>pVideoHandle</i> to <b>NULL</b> and return <b>E_NOTIMPL</b>.

If the protocol is not using the <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection.md">IWRdsRemoteFXGraphicsConnection</a> interface, this method should return a handle to the video miniport driver for the remote session associated with the protocol.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>