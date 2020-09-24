---
UID: NF:wsdclient.IWSDEventingStatus.SubscriptionRenewed
title: IWSDEventingStatus::SubscriptionRenewed (wsdclient.h)
description: Called when the subscription for the specified event action was successfully renewed.
helpviewer_keywords: ["IWSDEventingStatus interface","SubscriptionRenewed method","IWSDEventingStatus.SubscriptionRenewed","IWSDEventingStatus::SubscriptionRenewed","SubscriptionRenewed","SubscriptionRenewed method","SubscriptionRenewed method","IWSDEventingStatus interface","ncd.iwsdeventingstatus_subscriptionrenewed","wsdclient/IWSDEventingStatus::SubscriptionRenewed"]
old-location: ncd\iwsdeventingstatus_subscriptionrenewed.htm
tech.root: ncd
ms.assetid: 5f5c0b43-9c91-4d82-be98-1fd4fe7f9794
ms.date: 12/05/2018
ms.keywords: IWSDEventingStatus interface,SubscriptionRenewed method, IWSDEventingStatus.SubscriptionRenewed, IWSDEventingStatus::SubscriptionRenewed, SubscriptionRenewed, SubscriptionRenewed method, SubscriptionRenewed method,IWSDEventingStatus interface, ncd.iwsdeventingstatus_subscriptionrenewed, wsdclient/IWSDEventingStatus::SubscriptionRenewed
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDEventingStatus::SubscriptionRenewed
 - wsdclient/IWSDEventingStatus::SubscriptionRenewed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDEventingStatus.SubscriptionRenewed
---

# IWSDEventingStatus::SubscriptionRenewed


## -description

Called when the subscription for the specified event action was successfully renewed.

## -parameters

### -param pszSubscriptionAction [in]

URI of the event action.

## -remarks

After an operation is subscribed to, the service proxy will attempt to automatically renew the subscription until the client calls the appropriate <b>Unsubscribe</b> method or until the subscription is ended by the service. When the renewal succeeds, <b>SubscriptionRenewed</b> will be called to notify the client.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdeventingstatus">IWSDEventingStatus</a>