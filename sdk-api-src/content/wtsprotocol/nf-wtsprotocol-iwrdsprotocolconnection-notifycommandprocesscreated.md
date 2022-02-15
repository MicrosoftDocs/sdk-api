---
UID: NF:wtsprotocol.IWRdsProtocolConnection.NotifyCommandProcessCreated
title: IWRdsProtocolConnection::NotifyCommandProcessCreated (wtsprotocol.h)
description: Notifies the protocol that the Winlogon.exe process has been created and initialized.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","NotifyCommandProcessCreated method","IWRdsProtocolConnection.NotifyCommandProcessCreated","IWRdsProtocolConnection::NotifyCommandProcessCreated","NotifyCommandProcessCreated","NotifyCommandProcessCreated method [Remote Desktop Services]","NotifyCommandProcessCreated method [Remote Desktop Services]","IWRdsProtocolConnection interface","termserv.iwrdsprotocolconnection_notifycommandprocesscreated","wtsprotocol/IWRdsProtocolConnection::NotifyCommandProcessCreated"]
old-location: termserv\iwrdsprotocolconnection_notifycommandprocesscreated.htm
tech.root: TermServ
ms.assetid: B2A9CC5A-6E6E-418D-9C03-FDF207AFB683
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],NotifyCommandProcessCreated method, IWRdsProtocolConnection.NotifyCommandProcessCreated, IWRdsProtocolConnection::NotifyCommandProcessCreated, NotifyCommandProcessCreated, NotifyCommandProcessCreated method [Remote Desktop Services], NotifyCommandProcessCreated method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_notifycommandprocesscreated, wtsprotocol/IWRdsProtocolConnection::NotifyCommandProcessCreated
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
 - IWRdsProtocolConnection::NotifyCommandProcessCreated
 - wtsprotocol/IWRdsProtocolConnection::NotifyCommandProcessCreated
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
 - IWRdsProtocolConnection.NotifyCommandProcessCreated
---

# IWRdsProtocolConnection::NotifyCommandProcessCreated


## -description

Notifies the protocol that the Winlogon.exe process has been created and initialized.

## -parameters

### -param SessionId

The session identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>