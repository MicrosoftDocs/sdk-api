---
UID: NF:wtsprotocol.IWTSProtocolConnection.Close
title: IWTSProtocolConnection::Close (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnection::Close is no longer available. Instead, use IWRdsProtocolConnection::Close.
old-location: termserv\iwtsprotocolconnection_close.htm
tech.root: TermServ
ms.assetid: 746f5f06-7068-461b-8adf-b35d0c318942
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [Remote Desktop Services], Close method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],Close method, IWTSProtocolConnection.Close, IWTSProtocolConnection::Close, termserv.iwtsprotocolconnection_close, wtsprotocol/IWTSProtocolConnection::Close
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
 - IWTSProtocolConnection.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection::Close


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::Close</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-close">IWRdsProtocolConnection::Close</a>.]

Closes a connection after the session is disconnected.


## -parameters






## -remarks



 The protocol should perform whatever cleanup is necessary to close the connection and delete the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a>  object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>
 

 

