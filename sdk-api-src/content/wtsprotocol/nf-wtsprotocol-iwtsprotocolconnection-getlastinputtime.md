---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetLastInputTime
title: IWTSProtocolConnection::GetLastInputTime (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnection::GetLastInputTime is no longer available. Instead, use IWRdsProtocolConnection::GetLastInputTime.
old-location: termserv\iwtsprotocolconnection_getlastinputtime.htm
tech.root: TermServ
ms.assetid: 8daecbde-8866-4ae9-a07c-32d28d321392
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLastInputTime, GetLastInputTime method [Remote Desktop Services], GetLastInputTime method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetLastInputTime method, IWTSProtocolConnection.GetLastInputTime, IWTSProtocolConnection::GetLastInputTime, termserv.iwtsprotocolconnection_getlastinputtime, wtsprotocol/IWTSProtocolConnection::GetLastInputTime
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
 - IWTSProtocolConnection.GetLastInputTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnection::GetLastInputTime


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetLastInputTime</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/1a6acbd2-6155-4513-8892-50a4552abb12">IWRdsProtocolConnection::GetLastInputTime</a>.]

Returns the last time the protocol received input data.


## -parameters




### -param pLastInputTime [out]

An integer that contains the elapsed time, in milliseconds.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

