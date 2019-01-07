---
UID: NF:wtsprotocol.IWTSProtocolConnectionCallback.OnReady
title: IWTSProtocolConnectionCallback::OnReady
author: windows-sdk-content
description: IWTSProtocolConnectionCallback::OnReady is no longer available. Instead, use IWRdsProtocolConnectionCallback::OnReady.
old-location: termserv\iwtsprotocolconnectioncallback_onready.htm
tech.root: termserv
ms.assetid: a1289aca-bcf6-4fd2-a288-d401bece005d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWTSProtocolConnectionCallback interface [Remote Desktop Services],OnReady method, IWTSProtocolConnectionCallback.OnReady, IWTSProtocolConnectionCallback::OnReady, OnReady, OnReady method [Remote Desktop Services], OnReady method [Remote Desktop Services],IWTSProtocolConnectionCallback interface, termserv.iwtsprotocolconnectioncallback_onready, wtsprotocol/IWTSProtocolConnectionCallback::OnReady
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
 - IWTSProtocolConnectionCallback.OnReady
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolConnectionCallback::OnReady


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback::OnReady</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/88134a34-c494-48ea-9063-206e7d0c5139">IWRdsProtocolConnectionCallback::OnReady</a>.]

Requests that the Remote Desktop Services service continue the connection process for that client.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The protocol must call this method after the Remote Desktop Services service calls <a href="https://msdn.microsoft.com/b3fcc213-8257-433f-b304-ce19bc209591">SendPolicyData</a>. The Remote Desktop Services service will not call <a href="https://msdn.microsoft.com/5be00911-f68a-410d-8d56-81458b5ff44e">AcceptConnection</a> to continue the connection process until <b>OnReady</b> has been called.




## -see-also




<a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a>
 

 

