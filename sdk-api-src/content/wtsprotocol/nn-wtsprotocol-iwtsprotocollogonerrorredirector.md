---
UID: NN:wtsprotocol.IWTSProtocolLogonErrorRedirector
title: IWTSProtocolLogonErrorRedirector
author: windows-sdk-content
description: IWTSProtocolLogonErrorRedirector is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector.
old-location: termserv\iwtsprotocollogonerrorredirector.htm
old-project: TermServ
ms.assetid: 1ff30217-9091-47df-a38f-30784538f0b9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWTSProtocolLogonErrorRedirector, IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services], IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],described, termserv.iwtsprotocollogonerrorredirector, wtsprotocol/IWTSProtocolLogonErrorRedirector
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	wtsprotocol.h
api_name:
-	IWTSProtocolLogonErrorRedirector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolLogonErrorRedirector interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a>.]

Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages. This interface is implemented by the protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolLogonErrorRedirector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSProtocolLogonErrorRedirector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolLogonErrorRedirector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1356deeb-ac4a-4877-95be-9df09f4b0210">OnBeginPainting</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the logon user interface is ready to begin painting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10cd07c3-9617-4ef8-9b30-541a3206e7e4">RedirectLogonError</a>
</td>
<td align="left" width="63%">
Queries the protocol for the action to take in response to a logon error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8db3657c-f64f-4e38-832e-5808557f479d">RedirectMessage</a>
</td>
<td align="left" width="63%">
Queries the protocol regarding how to redirect the logon message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a333db5a-3564-4d33-bfd6-244975cc3c4f">RedirectStatus</a>
</td>
<td align="left" width="63%">
Queries the protocol regarding how to redirect the client logon status update.

</td>
</tr>
</table> 

