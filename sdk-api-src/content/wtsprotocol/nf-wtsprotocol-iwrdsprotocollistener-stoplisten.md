---
UID: NF:wtsprotocol.IWRdsProtocolListener.StopListen
title: IWRdsProtocolListener::StopListen
author: windows-sdk-content
description: Notifies the protocol to stop listening for client connection requests.
old-location: termserv\iwrdsprotocollistener_stoplisten.htm
tech.root: TermServ
ms.assetid: bfb758e8-3d71-47b9-bf7d-075c0c401177
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolListener interface [Remote Desktop Services],StopListen method, IWRdsProtocolListener.StopListen, IWRdsProtocolListener::StopListen, StopListen, StopListen method [Remote Desktop Services], StopListen method [Remote Desktop Services],IWRdsProtocolListener interface, termserv.iwrdsprotocollistener_stoplisten, wtsprotocol/IWRdsProtocolListener::StopListen
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolListener.StopListen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolListener::StopListen


## -description


Notifies the protocol to stop listening for client connection requests.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a>
 

 

