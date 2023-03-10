---
UID: NF:wtsprotocol.IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics
title: IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics (wtsprotocol.h)
description: Queries the protocol if RemoteFX graphics should be enabled for the connection.
helpviewer_keywords: ["EnableRemoteFXGraphics","EnableRemoteFXGraphics method [Remote Desktop Services]","EnableRemoteFXGraphics method [Remote Desktop Services]","IWRdsRemoteFXGraphicsConnection interface","IWRdsRemoteFXGraphicsConnection interface [Remote Desktop Services]","EnableRemoteFXGraphics method","IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics","IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics","termserv.iwrdsremotefxgraphicsconnection_enableremotefxgraphics","wtsprotocol/IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics"]
old-location: termserv\iwrdsremotefxgraphicsconnection_enableremotefxgraphics.htm
tech.root: TermServ
ms.assetid: 3ad667ed-bbb5-44e2-992a-df90bbab7b79
ms.date: 12/05/2018
ms.keywords: EnableRemoteFXGraphics, EnableRemoteFXGraphics method [Remote Desktop Services], EnableRemoteFXGraphics method [Remote Desktop Services],IWRdsRemoteFXGraphicsConnection interface, IWRdsRemoteFXGraphicsConnection interface [Remote Desktop Services],EnableRemoteFXGraphics method, IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics, IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics, termserv.iwrdsremotefxgraphicsconnection_enableremotefxgraphics, wtsprotocol/IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics
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
 - IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics
 - wtsprotocol/IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics
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
 - IWRdsRemoteFXGraphicsConnection.EnableRemoteFXGraphics
---

# IWRdsRemoteFXGraphicsConnection::EnableRemoteFXGraphics


## -description

<p class="CCE_Message">[The EnableRemoteFXGraphics method is deprecated and should not be used.
]

Queries the protocol if RemoteFX graphics should be enabled for the connection.

## -parameters

### -param pEnableRemoteFXGraphics [out]

The address of a <b>BOOL</b> variable that receives  <b>TRUE</b> to enable remote FX graphics; otherwise, <b>FALSE</b>.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection">IWRdsRemoteFXGraphicsConnection</a>