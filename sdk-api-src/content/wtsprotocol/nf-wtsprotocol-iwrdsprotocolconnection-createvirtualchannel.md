---
UID: NF:wtsprotocol.IWRdsProtocolConnection.CreateVirtualChannel
title: IWRdsProtocolConnection::CreateVirtualChannel (wtsprotocol.h)
description: Requests that the protocol create a virtual channel.
helpviewer_keywords: ["CreateVirtualChannel","CreateVirtualChannel method [Remote Desktop Services]","CreateVirtualChannel method [Remote Desktop Services]","IWRdsProtocolConnection interface","FALSE","IWRdsProtocolConnection interface [Remote Desktop Services]","CreateVirtualChannel method","IWRdsProtocolConnection.CreateVirtualChannel","IWRdsProtocolConnection::CreateVirtualChannel","TRUE","termserv.iwrdsprotocolconnection_createvirtualchannel","wtsprotocol/IWRdsProtocolConnection::CreateVirtualChannel"]
old-location: termserv\iwrdsprotocolconnection_createvirtualchannel.htm
tech.root: TermServ
ms.assetid: c0302081-06af-44af-a9ed-936d705e711b
ms.date: 12/05/2018
ms.keywords: CreateVirtualChannel, CreateVirtualChannel method [Remote Desktop Services], CreateVirtualChannel method [Remote Desktop Services],IWRdsProtocolConnection interface, FALSE, IWRdsProtocolConnection interface [Remote Desktop Services],CreateVirtualChannel method, IWRdsProtocolConnection.CreateVirtualChannel, IWRdsProtocolConnection::CreateVirtualChannel, TRUE, termserv.iwrdsprotocolconnection_createvirtualchannel, wtsprotocol/IWRdsProtocolConnection::CreateVirtualChannel
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
 - IWRdsProtocolConnection::CreateVirtualChannel
 - wtsprotocol/IWRdsProtocolConnection::CreateVirtualChannel
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
 - IWRdsProtocolConnection.CreateVirtualChannel
---

# IWRdsProtocolConnection::CreateVirtualChannel


## -description

Requests that the protocol create a virtual channel.

## -parameters

### -param szEndpointName [in]

A null-terminated string that contains the endpoint data that uniquely identifies the connection.

### -param bStatic [in]

Specifies whether the virtual channel is static or dynamic.



#### TRUE

The channel is static.



#### FALSE

The channel is dynamic.

### -param RequestedPriority [in]

Specifies the requested priority for the channel.

### -param phChannel [out]

A pointer to a <b>ULONG</b> value that receives the handle for the channel created.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Virtual channels are software extensions that can be created to enhance a Remote Desktop Services application. Examples include support for additional hardware or additions to the functionality provided by a given protocol. For more information, see <a href="/windows/desktop/TermServ/terminal-services-virtual-channels">Remote Desktop Services Virtual 
      Channels</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>