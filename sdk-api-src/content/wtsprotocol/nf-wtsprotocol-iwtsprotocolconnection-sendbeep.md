---
UID: NF:wtsprotocol.IWTSProtocolConnection.SendBeep
title: IWTSProtocolConnection::SendBeep
author: windows-sdk-content
description: IWTSProtocolConnection::SendBeep is no longer available.
old-location: termserv\iwtsprotocolconnection_sendbeep.htm
tech.root: termserv
ms.assetid: 4665917d-4bc3-4017-9b69-3eb95e70337f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],SendBeep method, IWTSProtocolConnection.SendBeep, IWTSProtocolConnection::SendBeep, SendBeep, SendBeep method [Remote Desktop Services], SendBeep method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_sendbeep, wtsprotocol/IWTSProtocolConnection::SendBeep
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolConnection.SendBeep
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

