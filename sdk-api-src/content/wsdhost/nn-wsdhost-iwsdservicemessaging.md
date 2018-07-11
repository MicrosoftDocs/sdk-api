---
UID: NN:wsdhost.IWSDServiceMessaging
title: IWSDServiceMessaging
author: windows-sdk-content
description: Is used by generated stub code to send faults or responses to incoming messages.
old-location: ncd\iwsdservicemessaging.htm
old-project: wsdapi
ms.assetid: 06584474-1c55-43db-9c7a-fefea8d16eed
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: IWSDServiceMessaging, IWSDServiceMessaging interface, IWSDServiceMessaging interface,described, ncd.iwsdservicemessaging, wsdhost/IWSDServiceMessaging
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceMessaging
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceMessaging interface


## -description


The <b>IWSDServiceMessaging</b> interface is used by generated stub code to send faults or responses to incoming messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDServiceMessaging</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDServiceMessaging</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDServiceMessaging</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/478cf63e-7cfe-4f6f-af7f-d288588d9c8d">FaultRequest</a>
</td>
<td align="left" width="63%">
Sends a fault matching a given request context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec136c44-b8f5-42db-a965-2dd5b3cd18ad">SendResponse</a>
</td>
<td align="left" width="63%">
Sends a response message matching a given request context.

</td>
</tr>
</table> 

