---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetLogonErrorRedirector
title: IWRdsProtocolConnection::GetLogonErrorRedirector
author: windows-sdk-content
description: Retrieves an IWRdsProtocolLogonErrorRedirector interface that specifies how the protocol should handle client logon errors.
old-location: termserv\iwrdsprotocolconnection_getlogonerrorredirector.htm
old-project: termserv
ms.assetid: 9613330F-B8DE-48C7-892C-FB8F50739C13
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: GetLogonErrorRedirector, GetLogonErrorRedirector method [Remote Desktop Services], GetLogonErrorRedirector method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetLogonErrorRedirector method, IWRdsProtocolConnection.GetLogonErrorRedirector, IWRdsProtocolConnection::GetLogonErrorRedirector, termserv.iwrdsprotocolconnection_getlogonerrorredirector, wtsprotocol/IWRdsProtocolConnection::GetLogonErrorRedirector
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
 - IWRdsProtocolConnection.GetLogonErrorRedirector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::GetLogonErrorRedirector


## -description


Retrieves an <a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors. The protocol must add a reference to this object before returning, and the Remote Desktop Services service releases the reference when the connection is closed.


## -parameters




### -param ppLogonErrorRedir [out]

Address of a pointer to an <a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a> interface.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

If you do not implement this function, return <b>E_NOTIMPL</b> to indicate that logon errors should not be redirected. 




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

