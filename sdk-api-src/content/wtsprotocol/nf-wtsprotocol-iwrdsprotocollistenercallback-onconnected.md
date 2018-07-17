---
UID: NF:wtsprotocol.IWRdsProtocolListenerCallback.OnConnected
title: IWRdsProtocolListenerCallback::OnConnected
author: windows-sdk-content
description: Notifies the Remote Desktop Services service that a client connection request has been received.
old-location: termserv\iwrdsprotocollistenercallback_onconnected.htm
old-project: termserv
ms.assetid: 9d2d5393-f0a6-40ec-9bf2-2e8c945693db
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWRdsProtocolListenerCallback interface [Remote Desktop Services],OnConnected method, IWRdsProtocolListenerCallback.OnConnected, IWRdsProtocolListenerCallback::OnConnected, OnConnected, OnConnected method [Remote Desktop Services], OnConnected method [Remote Desktop Services],IWRdsProtocolListenerCallback interface, termserv.iwrdsprotocollistenercallback_onconnected, wtsprotocol/IWRdsProtocolListenerCallback::OnConnected
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolListenerCallback.OnConnected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolListenerCallback::OnConnected


## -description


Notifies the Remote Desktop Services service that a client connection request has been received. 
 After this method is called, the Remote Desktop Services service begins the client connection sequence.


## -parameters




### -param pConnection [in]

A pointer to an <a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a> interface that represents a client connection. The Remote Desktop Services service  adds a reference to this object and releases it when it closes the connection.


### -param pWRdsConnectionSettings [in]

A pointer to a <a href="https://msdn.microsoft.com/9219AE45-5F11-484E-BD78-F8E1AB41D648">WRDS_CONNECTION_SETTINGS</a> structure that contains the connection settings for the remote session.


### -param pCallback [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/81a73688-f39e-4960-8587-602d56c11e7e">IWRdsProtocolConnectionCallback</a> interface used by the protocol to notify the Remote Desktop Services service about the status of a client connection. The Remote Desktop Services service  adds a reference to this object and the protocol must release it when the connection is closed.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/33f583a4-8311-4db1-9646-bed1cd06e479">IWRdsProtocolListenerCallback</a>
 

 

