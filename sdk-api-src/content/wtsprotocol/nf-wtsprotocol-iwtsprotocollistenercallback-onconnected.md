---
UID: NF:wtsprotocol.IWTSProtocolListenerCallback.OnConnected
title: IWTSProtocolListenerCallback::OnConnected (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolListenerCallback::OnConnected is no longer available. Instead, use IWRdsProtocolListenerCallback::OnConnected.
old-location: termserv\iwtsprotocollistenercallback_onconnected.htm
tech.root: TermServ
ms.assetid: 0874c394-6260-4ac1-b5a8-27879f562e19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolListenerCallback interface [Remote Desktop Services],OnConnected method, IWTSProtocolListenerCallback.OnConnected, IWTSProtocolListenerCallback::OnConnected, OnConnected, OnConnected method [Remote Desktop Services], OnConnected method [Remote Desktop Services],IWTSProtocolListenerCallback interface, termserv.iwtsprotocollistenercallback_onconnected, wtsprotocol/IWTSProtocolListenerCallback::OnConnected
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
 - IWTSProtocolListenerCallback.OnConnected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolListenerCallback::OnConnected


## -description


<p class="CCE_Message">[<b>IWTSProtocolListenerCallback::OnConnected</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/9d2d5393-f0a6-40ec-9bf2-2e8c945693db">IWRdsProtocolListenerCallback::OnConnected</a>.]

Notifies the Remote Desktop Services service that a client connection request has been received. 
 After this method is called, the Remote Desktop Services service begins the client connection sequence.


## -parameters




### -param pConnection [in]

A pointer to an <a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a> interface that represents a client connection. The Remote Desktop Services service  adds a reference to this object and releases it when it closes the connection.


### -param pCallback [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a> interface used by the protocol to notify the Remote Desktop Services service about the status of a client connection. The Remote Desktop Services service  adds a reference to this object and the protocol must release it when the connection is closed.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/607fcb85-4602-4651-b246-3e32c8868e47">IWTSProtocolListenerCallback</a>
 

 

