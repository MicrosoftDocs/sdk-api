---
UID: NF:wtsprotocol.IWTSProtocolConnection.CreateVirtualChannel
title: IWTSProtocolConnection::CreateVirtualChannel
author: windows-sdk-content
description: IWTSProtocolConnection::CreateVirtualChannel is no longer available. Instead, use IWRdsProtocolConnection::CreateVirtualChannel.
old-location: termserv\iwtsprotocolconnection_createvirtualchannel.htm
tech.root: TermServ
ms.assetid: 28cdabde-980f-48b7-920e-1eeeb70b6952
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateVirtualChannel, CreateVirtualChannel method [Remote Desktop Services], CreateVirtualChannel method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],CreateVirtualChannel method, IWTSProtocolConnection.CreateVirtualChannel, IWTSProtocolConnection::CreateVirtualChannel, termserv.iwtsprotocolconnection_createvirtualchannel, wtsprotocol/IWTSProtocolConnection::CreateVirtualChannel
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
 - IWTSProtocolConnection.CreateVirtualChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnection::CreateVirtualChannel


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::CreateVirtualChannel</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/c0302081-06af-44af-a9ed-936d705e711b">IWRdsProtocolConnection::CreateVirtualChannel</a>.]

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



Virtual channels are software extensions that can be created to enhance a Remote Desktop Services application. Examples include support for additional hardware or additions to the functionality provided by a given protocol. For more information, see <a href="https://msdn.microsoft.com/f7bdebec-ecc3-4f28-9327-f0d2f169c142">Remote Desktop Services Virtual 
      Channels</a>.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

