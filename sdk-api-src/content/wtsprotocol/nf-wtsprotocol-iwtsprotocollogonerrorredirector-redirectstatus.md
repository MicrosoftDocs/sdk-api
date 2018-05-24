---
UID: NF:wtsprotocol.IWTSProtocolLogonErrorRedirector.RedirectStatus
title: IWTSProtocolLogonErrorRedirector::RedirectStatus
author: windows-driver-content
description: IWTSProtocolLogonErrorRedirector::RedirectStatus is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector::RedirectStatus.
old-location: termserv\iwtsprotocollogonerrorredirector_redirectstatus.htm
old-project: TermServ
ms.assetid: a333db5a-3564-4d33-bfd6-244975cc3c4f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectStatus method, IWTSProtocolLogonErrorRedirector.RedirectStatus, IWTSProtocolLogonErrorRedirector::RedirectStatus, RedirectStatus, RedirectStatus method [Remote Desktop Services], RedirectStatus method [Remote Desktop Services],IWTSProtocolLogonErrorRedirector interface, termserv.iwtsprotocollogonerrorredirector_redirectstatus, wtsprotocol/IWTSProtocolLogonErrorRedirector::RedirectStatus
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wtsprotocol.h
api_name:
-	IWTSProtocolLogonErrorRedirector.RedirectStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolLogonErrorRedirector::RedirectStatus


## -description


<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector::RedirectStatus</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/f1f6caec-6e26-4508-b19d-ac0e12758b28">IWRdsProtocolLogonErrorRedirector::RedirectStatus</a>.]

Queries the protocol regarding how to redirect the client logon status update.


## -parameters




### -param pszMessage [in]

A pointer to a string that contains the logon status message.


### -param pResponse [out]

A pointer to a <a href="https://msdn.microsoft.com/67ed8d6f-641c-4739-911c-e61379e14048">WTS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that contains the response. This can be one of the following values.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/1ff30217-9091-47df-a38f-30784538f0b9">IWTSProtocolLogonErrorRedirector</a>
 

 

