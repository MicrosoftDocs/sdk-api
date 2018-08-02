---
UID: NF:wtsprotocol.IWRdsProtocolConnection.CreateVirtualChannel
title: IWRdsProtocolConnection::CreateVirtualChannel
author: windows-sdk-content
description: Requests that the protocol create a virtual channel.
old-location: termserv\iwrdsprotocolconnection_createvirtualchannel.htm
old-project: TermServ
ms.assetid: c0302081-06af-44af-a9ed-936d705e711b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateVirtualChannel, CreateVirtualChannel method [Remote Desktop Services], CreateVirtualChannel method [Remote Desktop Services],IWRdsProtocolConnection interface, FALSE, IWRdsProtocolConnection interface [Remote Desktop Services],CreateVirtualChannel method, IWRdsProtocolConnection.CreateVirtualChannel, IWRdsProtocolConnection::CreateVirtualChannel, TRUE, termserv.iwrdsprotocolconnection_createvirtualchannel, wtsprotocol/IWRdsProtocolConnection::CreateVirtualChannel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWRdsProtocolConnection.CreateVirtualChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Virtual channels are software extensions that can be created to enhance a Remote Desktop Services application. Examples include support for additional hardware or additions to the functionality provided by a given protocol. For more information, see <a href="https://msdn.microsoft.com/f7bdebec-ecc3-4f28-9327-f0d2f169c142">Remote Desktop Services Virtual 
      Channels</a>.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

