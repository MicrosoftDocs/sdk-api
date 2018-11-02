---
UID: NF:wtsprotocol.IWTSProtocolListener.StopListen
title: IWTSProtocolListener::StopListen
author: windows-sdk-content
description: IWTSProtocolListener::StopListen is no longer available. Instead, use IWRdsProtocolListener::StopListen.
old-location: termserv\iwtsprotocollistener_stoplisten.htm
tech.root: termserv
ms.assetid: 5c5b09d3-74d6-4067-b18b-ed2a54af4153
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWTSProtocolListener interface [Remote Desktop Services],StopListen method, IWTSProtocolListener.StopListen, IWTSProtocolListener::StopListen, StopListen, StopListen method [Remote Desktop Services], StopListen method [Remote Desktop Services],IWTSProtocolListener interface, termserv.iwtsprotocollistener_stoplisten, wtsprotocol/IWTSProtocolListener::StopListen
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
 - IWTSProtocolListener.StopListen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolListener::StopListen


## -description


<p class="CCE_Message">[<b>IWTSProtocolListener::StopListen</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/bfb758e8-3d71-47b9-bf7d-075c0c401177">IWRdsProtocolListener::StopListen</a>.]

Notifies the protocol to stop listening for client connection requests.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a>
 

 

