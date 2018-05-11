---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetLastInputTime
title: IWRdsProtocolConnection::GetLastInputTime
author: windows-driver-content
description: Retrieves the last time the protocol received user input.
old-location: termserv\iwrdsprotocolconnection_getlastinputtime.htm
old-project: TermServ
ms.assetid: 1a6acbd2-6155-4513-8892-50a4552abb12
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetLastInputTime, GetLastInputTime method [Remote Desktop Services], GetLastInputTime method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetLastInputTime method, IWRdsProtocolConnection.GetLastInputTime, IWRdsProtocolConnection::GetLastInputTime, termserv.iwrdsprotocolconnection_getlastinputtime, wtsprotocol/IWRdsProtocolConnection::GetLastInputTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWRdsProtocolConnection.GetLastInputTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::GetLastInputTime


## -description


Retrieves the last time the protocol received user input.


## -parameters




### -param pLastInputTime [out]

A pointer to a <b>ULONG64</b> value that receives the number of milliseconds that has elapsed since the protocol last received input.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

