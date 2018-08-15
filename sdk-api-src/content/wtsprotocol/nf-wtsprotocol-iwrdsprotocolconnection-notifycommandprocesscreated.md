---
UID: NF:wtsprotocol.IWRdsProtocolConnection.NotifyCommandProcessCreated
title: IWRdsProtocolConnection::NotifyCommandProcessCreated
author: windows-sdk-content
description: Notifies the protocol that the Winlogon.exe process has been created and initialized.
old-location: termserv\iwrdsprotocolconnection_notifycommandprocesscreated.htm
old-project: termserv
ms.assetid: B2A9CC5A-6E6E-418D-9C03-FDF207AFB683
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],NotifyCommandProcessCreated method, IWRdsProtocolConnection.NotifyCommandProcessCreated, IWRdsProtocolConnection::NotifyCommandProcessCreated, NotifyCommandProcessCreated, NotifyCommandProcessCreated method [Remote Desktop Services], NotifyCommandProcessCreated method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_notifycommandprocesscreated, wtsprotocol/IWRdsProtocolConnection::NotifyCommandProcessCreated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.NotifyCommandProcessCreated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::NotifyCommandProcessCreated


## -description


Notifies the protocol that the Winlogon.exe process has been created and initialized.


## -parameters




### -param SessionId

The session identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

