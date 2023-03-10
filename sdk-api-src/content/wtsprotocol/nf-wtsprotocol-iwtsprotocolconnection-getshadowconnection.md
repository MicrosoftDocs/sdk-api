---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetShadowConnection
title: IWTSProtocolConnection::GetShadowConnection (wtsprotocol.h)
description: IWTSProtocolConnection::GetShadowConnection is no longer available. Instead, use IWRdsProtocolConnection::GetShadowConnection.
helpviewer_keywords: ["GetShadowConnection","GetShadowConnection method [Remote Desktop Services]","GetShadowConnection method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetShadowConnection method","IWTSProtocolConnection.GetShadowConnection","IWTSProtocolConnection::GetShadowConnection","termserv.iwtsprotocolconnection_getshadowconnection","wtsprotocol/IWTSProtocolConnection::GetShadowConnection"]
old-location: termserv\iwtsprotocolconnection_getshadowconnection.htm
tech.root: TermServ
ms.assetid: 6496deba-6166-48d2-9294-286a448de231
ms.date: 12/05/2018
ms.keywords: GetShadowConnection, GetShadowConnection method [Remote Desktop Services], GetShadowConnection method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetShadowConnection method, IWTSProtocolConnection.GetShadowConnection, IWTSProtocolConnection::GetShadowConnection, termserv.iwtsprotocolconnection_getshadowconnection, wtsprotocol/IWTSProtocolConnection::GetShadowConnection
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IWTSProtocolConnection::GetShadowConnection
 - wtsprotocol/IWTSProtocolConnection::GetShadowConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.GetShadowConnection
---

# IWTSProtocolConnection::GetShadowConnection


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetShadowConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getshadowconnection">IWRdsProtocolConnection::GetShadowConnection</a>.]

Retrieves a  <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection">IWTSProtocolShadowConnection</a> object from the protocol. The method must add a reference to the object before returning. When the Remote Desktop Services service has finished the licensing process, it will release the reference.

## -parameters

### -param ppShadowConnection [out]

 The address of a pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection">IWTSProtocolShadowConnection</a> interface.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>