---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.OnReady
title: IWRdsProtocolConnectionCallback::OnReady
author: windows-driver-content
description: Requests that the Remote Desktop Services service continue the connection process for that client.
old-location: termserv\iwrdsprotocolconnectioncallback_onready.htm
old-project: TermServ
ms.assetid: 88134a34-c494-48ea-9063-206e7d0c5139
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IWRdsProtocolConnectionCallback interface [Remote Desktop Services],OnReady method, IWRdsProtocolConnectionCallback.OnReady, IWRdsProtocolConnectionCallback::OnReady, OnReady, OnReady method [Remote Desktop Services], OnReady method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, termserv.iwrdsprotocolconnectioncallback_onready, wtsprotocol/IWRdsProtocolConnectionCallback::OnReady
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
-	IWRdsProtocolConnectionCallback.OnReady
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnectionCallback::OnReady


## -description


Requests that the Remote Desktop Services service continue the connection process for that client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The protocol must call this method after the Remote Desktop Services service calls <a href="https://msdn.microsoft.com/9613330F-B8DE-48C7-892C-FB8F50739C13">GetLogonErrorRedirector</a>. The Remote Desktop Services service will not call <a href="https://msdn.microsoft.com/ef7e13ad-eeb8-4452-b3d6-a137b766f98f">AcceptConnection</a> to continue the connection process until <b>OnReady</b> has been called.




## -see-also




<a href="https://msdn.microsoft.com/81a73688-f39e-4960-8587-602d56c11e7e">IWRdsProtocolConnectionCallback</a>
 

 

