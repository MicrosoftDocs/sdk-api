---
UID: NF:wtsprotocol.IWTSProtocolConnection.CreateVirtualChannel
title: IWTSProtocolConnection::CreateVirtualChannel (wtsprotocol.h)
description: IWTSProtocolConnection::CreateVirtualChannel is no longer available. Instead, use IWRdsProtocolConnection::CreateVirtualChannel.
helpviewer_keywords: ["CreateVirtualChannel","CreateVirtualChannel method [Remote Desktop Services]","CreateVirtualChannel method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","CreateVirtualChannel method","IWTSProtocolConnection.CreateVirtualChannel","IWTSProtocolConnection::CreateVirtualChannel","termserv.iwtsprotocolconnection_createvirtualchannel","wtsprotocol/IWTSProtocolConnection::CreateVirtualChannel"]
old-location: termserv\iwtsprotocolconnection_createvirtualchannel.htm
tech.root: TermServ
ms.assetid: 28cdabde-980f-48b7-920e-1eeeb70b6952
ms.date: 12/05/2018
ms.keywords: CreateVirtualChannel, CreateVirtualChannel method [Remote Desktop Services], CreateVirtualChannel method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],CreateVirtualChannel method, IWTSProtocolConnection.CreateVirtualChannel, IWTSProtocolConnection::CreateVirtualChannel, termserv.iwtsprotocolconnection_createvirtualchannel, wtsprotocol/IWTSProtocolConnection::CreateVirtualChannel
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
 - IWTSProtocolConnection::CreateVirtualChannel
 - wtsprotocol/IWTSProtocolConnection::CreateVirtualChannel
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
 - IWTSProtocolConnection.CreateVirtualChannel
---

# IWTSProtocolConnection::CreateVirtualChannel


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::CreateVirtualChannel</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-createvirtualchannel">IWRdsProtocolConnection::CreateVirtualChannel</a>.]

Creates a static or dynamic virtual channel.

## -parameters

### -param szEndpointName [in]

A string value that contains the endpoint data that uniquely identifies the connection.

### -param bStatic [in]

A Boolean value that specifies whether the virtual channel is static or dynamic. A value of <b>TRUE</b> specifies a static channel.

### -param RequestedPriority [in]

An integer that contains the priority.

### -param phChannel [out]

A pointer to the channel handle.

## -remarks

Virtual channels are software extensions that can be created to enhance a Remote Desktop Services application. Examples include support for additional hardware or additions to the functionality provided by a given protocol. For more information, see <a href="/windows/desktop/TermServ/terminal-services-virtual-channels">Remote Desktop Services Virtual 
      Channels</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>