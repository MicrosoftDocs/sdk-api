---
UID: NN:wtsprotocol.IWRdsProtocolShadowCallback
title: IWRdsProtocolShadowCallback
author: windows-sdk-content
description: Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.
old-location: termserv\iwrdsprotocolshadowcallback.htm
old-project: TermServ
ms.assetid: 47727d33-df3d-49da-bc82-a4ed5ce0a381
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWRdsProtocolShadowCallback, IWRdsProtocolShadowCallback interface [Remote Desktop Services], IWRdsProtocolShadowCallback interface [Remote Desktop Services],described, termserv.iwrdsprotocolshadowcallback, wtsprotocol/IWRdsProtocolShadowCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IWRdsProtocolShadowCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolShadowCallback interface


## -description


 Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow. This interface is the callback interface for the <a href="https://msdn.microsoft.com/d23c4902-4e61-45ff-8a49-62eea1b92d4a">IWRdsProtocolShadowConnection</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolShadowCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolShadowCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolShadowCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76682f4c-2651-4f5d-b96d-4d84bae7933c">InvokeTargetShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09911813-554d-4ce1-b34e-5a6f57ec286d">StopShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to stop shadowing a target.

</td>
</tr>
</table> 

