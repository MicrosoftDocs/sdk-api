---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetClientMonitorData
title: IWRdsProtocolConnection::GetClientMonitorData
author: windows-sdk-content
description: Retrieves the number of monitors and the primary monitor number on the client.
old-location: termserv\iwrdsprotocolconnection_getclientmonitordata.htm
old-project: TermServ
ms.assetid: df70ff56-3e12-4842-a818-31ee75da96a9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetClientMonitorData, GetClientMonitorData method [Remote Desktop Services], GetClientMonitorData method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetClientMonitorData method, IWRdsProtocolConnection.GetClientMonitorData, IWRdsProtocolConnection::GetClientMonitorData, termserv.iwrdsprotocolconnection_getclientmonitordata, termserv.iwrdsremotefxgraphicsconnection_getclientmonitordata, wtsprotocol/IWRdsProtocolConnection::GetClientMonitorData
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWRdsProtocolConnection.GetClientMonitorData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::GetClientMonitorData


## -description


Retrieves the number of monitors and the primary monitor number on the client.


## -parameters




### -param pNumMonitors [out]

A pointer to a <b>UINT</b> variable to receive the number of monitors counted.


### -param pPrimaryMonitor [out]

A pointer to a <b>UINT</b> variable to receive the number of the primary monitor on the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

