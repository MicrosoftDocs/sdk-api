---
UID: NN:wsdclient.IWSDEventingStatus
title: IWSDEventingStatus
author: windows-driver-content
description: Implement this interface to receive notification when status changes occur in event subscriptions.
old-location: ncd\iwsdeventingstatus.htm
old-project: WsdApi
ms.assetid: 04e6ea03-f9b5-48d9-940f-532bb3a85ff0
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IWSDEventingStatus, IWSDEventingStatus interface, IWSDEventingStatus interface,described, ncd.iwsdeventingstatus, wsdclient/IWSDEventingStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDEventingStatus
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDEventingStatus interface


## -description


Implement this interface to receive notification when status changes occur in event subscriptions. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDEventingStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDEventingStatus</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4ccb16ed-d7c6-4242-ae53-9e58cecc475b">SubscriptionEnded</a>
</td>
<td align="left" width="63%">
Indicates that subscription has been terminated by the subscription manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d76bb6ae-bb4d-4226-be0d-4fd37b0212a9">SubscriptionRenewalFailed</a>
</td>
<td align="left" width="63%">
Indicates that the service proxy was unable to renew the subscription with the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f5c0b43-9c91-4d82-be98-1fd4fe7f9794">SubscriptionRenewed</a>
</td>
<td align="left" width="63%">
Indicates that the subscription has successfully been renewed.

</td>
</tr>
</table> 

