---
UID: NN:wsdclient.IWSDEventingStatus
title: IWSDEventingStatus (wsdclient.h)
description: Implement this interface to receive notification when status changes occur in event subscriptions.
old-location: ncd\iwsdeventingstatus.htm
tech.root: WsdApi
ms.assetid: 04e6ea03-f9b5-48d9-940f-532bb3a85ff0
ms.date: 12/05/2018
ms.keywords: IWSDEventingStatus, IWSDEventingStatus interface, IWSDEventingStatus interface,described, ncd.iwsdeventingstatus, wsdclient/IWSDEventingStatus
ms.topic: interface
f1_keywords:
- wsdclient/IWSDEventingStatus
dev_langs:
- c++
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsdapi.dll
api_name:
- IWSDEventingStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDEventingStatus interface


## -description


Implement this interface to receive notification when status changes occur in event subscriptions. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDEventingStatus</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDEventingStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDEventingStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdeventingstatus-subscriptionended">SubscriptionEnded</a>
</td>
<td align="left" width="63%">
Indicates that subscription has been terminated by the subscription manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdeventingstatus-subscriptionrenewalfailed">SubscriptionRenewalFailed</a>
</td>
<td align="left" width="63%">
Indicates that the service proxy was unable to renew the subscription with the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdeventingstatus-subscriptionrenewed">SubscriptionRenewed</a>
</td>
<td align="left" width="63%">
Indicates that the subscription has successfully been renewed.

</td>
</tr>
</table> 

