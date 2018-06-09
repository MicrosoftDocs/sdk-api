---
UID: NN:wtsprotocol.IWTSProtocolShadowCallback
title: IWTSProtocolShadowCallback
author: windows-sdk-content
description: IWTSProtocolShadowCallback is no longer available. Instead, use IWRdsProtocolShadowCallback.
old-location: termserv\iwtsprotocolshadowcallback.htm
old-project: TermServ
ms.assetid: ce224b9f-161c-4133-97d9-05c339eefb77
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWTSProtocolShadowCallback, IWTSProtocolShadowCallback interface [Remote Desktop Services], IWTSProtocolShadowCallback interface [Remote Desktop Services],described, termserv.iwtsprotocolshadowcallback, wtsprotocol/IWTSProtocolShadowCallback
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
 - IWTSProtocolShadowCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolShadowCallback interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowCallback</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/47727d33-df3d-49da-bc82-a4ed5ce0a381">IWRdsProtocolShadowCallback</a>.]

 Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow. This interface is the callback interface for the <a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolShadowCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSProtocolShadowCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolShadowCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ce090cd-6824-4a89-acb4-138a1d0f6f76">InvokeTargetShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54e47922-aea5-4e2f-b329-94300fc1ac3d">StopShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to stop shadowing a target.

</td>
</tr>
</table> 

