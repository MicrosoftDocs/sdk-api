---
UID: NN:wsdhost.IWSDServiceMessaging
title: IWSDServiceMessaging (wsdhost.h)
description: Is used by generated stub code to send faults or responses to incoming messages.
helpviewer_keywords: ["IWSDServiceMessaging","IWSDServiceMessaging interface","IWSDServiceMessaging interface","described","ncd.iwsdservicemessaging","wsdhost/IWSDServiceMessaging"]
old-location: ncd\iwsdservicemessaging.htm
tech.root: ncd
ms.assetid: 06584474-1c55-43db-9c7a-fefea8d16eed
ms.date: 12/05/2018
ms.keywords: IWSDServiceMessaging, IWSDServiceMessaging interface, IWSDServiceMessaging interface,described, ncd.iwsdservicemessaging, wsdhost/IWSDServiceMessaging
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDServiceMessaging
 - wsdhost/IWSDServiceMessaging
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceMessaging
---

# IWSDServiceMessaging interface


## -description

The <b>IWSDServiceMessaging</b> interface is used by generated stub code to send faults or responses to incoming messages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDServiceMessaging</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDServiceMessaging</b> also has these types of members:
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
<a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsdservicemessaging-faultrequest">FaultRequest</a>
</td>
<td align="left" width="63%">
Sends a fault matching a given request context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsdservicemessaging-sendresponse">SendResponse</a>
</td>
<td align="left" width="63%">
Sends a response message matching a given request context.

</td>
</tr>
</table>