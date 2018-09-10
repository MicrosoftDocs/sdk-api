---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetProtocolStatus
title: IWTSProtocolConnection::GetProtocolStatus
author: windows-sdk-content
description: IWTSProtocolConnection::GetProtocolStatus is no longer available. Instead, use IWRdsProtocolConnection::GetProtocolStatus.
old-location: termserv\iwtsprotocolconnection_getprotocolstatus.htm
tech.root: termserv
ms.assetid: d224877a-649a-4ac2-a5e7-831592e6a0d9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetProtocolStatus, GetProtocolStatus method [Remote Desktop Services], GetProtocolStatus method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetProtocolStatus method, IWTSProtocolConnection.GetProtocolStatus, IWTSProtocolConnection::GetProtocolStatus, termserv.iwtsprotocolconnection_getprotocolstatus, wtsprotocol/IWTSProtocolConnection::GetProtocolStatus
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
 - IWTSProtocolConnection.GetProtocolStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnection::GetProtocolStatus


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetProtocolStatus</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/A89C2E3F-AC75-4CFB-9DA7-00DCEDCA1C1A">IWRdsProtocolConnection::GetProtocolStatus</a>.]

Retrieves information about the protocol status.


## -parameters




### -param pProtocolStatus [out]

A pointer to a <a href="https://msdn.microsoft.com/20e66033-fc79-49c9-af0e-abaf6e4ba501">WTS_PROTOCOL_STATUS</a> structure that contains counter, signal, and cache information for the protocol.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

