---
UID: NF:wtsprotocol.IWRdsProtocolLogonErrorRedirector.OnBeginPainting
title: IWRdsProtocolLogonErrorRedirector::OnBeginPainting
author: windows-sdk-content
description: Notifies the protocol that the logon user interface is ready to begin painting.
old-location: termserv\iwrdsprotocollogonerrorredirector_onbeginpainting.htm
old-project: termserv
ms.assetid: cc044746-1127-44a3-993d-ca2445c99ff6
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],OnBeginPainting method, IWRdsProtocolLogonErrorRedirector.OnBeginPainting, IWRdsProtocolLogonErrorRedirector::OnBeginPainting, OnBeginPainting, OnBeginPainting method [Remote Desktop Services], OnBeginPainting method [Remote Desktop Services],IWRdsProtocolLogonErrorRedirector interface, termserv.iwrdsprotocollogonerrorredirector_onbeginpainting, wtsprotocol/IWRdsProtocolLogonErrorRedirector::OnBeginPainting
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
 - IWRdsProtocolLogonErrorRedirector.OnBeginPainting
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolLogonErrorRedirector::OnBeginPainting


## -description


Notifies the protocol that the logon user interface is ready to begin painting.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a>
 

 

