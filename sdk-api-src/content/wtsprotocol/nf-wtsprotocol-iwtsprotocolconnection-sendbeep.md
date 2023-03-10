---
UID: NF:wtsprotocol.IWTSProtocolConnection.SendBeep
title: IWTSProtocolConnection::SendBeep (wtsprotocol.h)
description: IWTSProtocolConnection::SendBeep is no longer available.
helpviewer_keywords: ["IWTSProtocolConnection interface [Remote Desktop Services]","SendBeep method","IWTSProtocolConnection.SendBeep","IWTSProtocolConnection::SendBeep","SendBeep","SendBeep method [Remote Desktop Services]","SendBeep method [Remote Desktop Services]","IWTSProtocolConnection interface","termserv.iwtsprotocolconnection_sendbeep","wtsprotocol/IWTSProtocolConnection::SendBeep"]
old-location: termserv\iwtsprotocolconnection_sendbeep.htm
tech.root: TermServ
ms.assetid: 4665917d-4bc3-4017-9b69-3eb95e70337f
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],SendBeep method, IWTSProtocolConnection.SendBeep, IWTSProtocolConnection::SendBeep, SendBeep, SendBeep method [Remote Desktop Services], SendBeep method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_sendbeep, wtsprotocol/IWTSProtocolConnection::SendBeep
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
 - IWTSProtocolConnection::SendBeep
 - wtsprotocol/IWTSProtocolConnection::SendBeep
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
 - IWTSProtocolConnection.SendBeep
---

# IWTSProtocolConnection::SendBeep


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::SendBeep</b> is no longer available for use as of Windows Server 2012.]

Sends a sound pulse to the console speaker on the client.

The beep() function does not cause <b>SendBeep</b> to be called. To work around this issue, the user must enable Remote Desktop Services audio redirection capabilities to remotely hear beep sounds.

## -parameters

### -param Frequency [in]

An integer that contains the pulse frequency ranging from 37 to 32,767 Hertz.

### -param Duration [in]

An integer that contains the pulse duration, in milliseconds.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>