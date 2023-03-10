---
UID: NF:wsdclient.IWSDEventingStatus.SubscriptionRenewalFailed
title: IWSDEventingStatus::SubscriptionRenewalFailed (wsdclient.h)
description: Called when the subscription for the specified event action could not be renewed.
helpviewer_keywords: ["IWSDEventingStatus interface","SubscriptionRenewalFailed method","IWSDEventingStatus.SubscriptionRenewalFailed","IWSDEventingStatus::SubscriptionRenewalFailed","SubscriptionRenewalFailed","SubscriptionRenewalFailed method","SubscriptionRenewalFailed method","IWSDEventingStatus interface","ncd.iwsdeventingstatus_subscriptionrenewalfailed","wsdclient/IWSDEventingStatus::SubscriptionRenewalFailed"]
old-location: ncd\iwsdeventingstatus_subscriptionrenewalfailed.htm
tech.root: ncd
ms.assetid: d76bb6ae-bb4d-4226-be0d-4fd37b0212a9
ms.date: 12/05/2018
ms.keywords: IWSDEventingStatus interface,SubscriptionRenewalFailed method, IWSDEventingStatus.SubscriptionRenewalFailed, IWSDEventingStatus::SubscriptionRenewalFailed, SubscriptionRenewalFailed, SubscriptionRenewalFailed method, SubscriptionRenewalFailed method,IWSDEventingStatus interface, ncd.iwsdeventingstatus_subscriptionrenewalfailed, wsdclient/IWSDEventingStatus::SubscriptionRenewalFailed
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
 - IWSDEventingStatus::SubscriptionRenewalFailed
 - wsdclient/IWSDEventingStatus::SubscriptionRenewalFailed
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
 - IWSDEventingStatus.SubscriptionRenewalFailed
---

# IWSDEventingStatus::SubscriptionRenewalFailed


## -description

Called when the subscription for the specified event action could not be renewed.

## -parameters

### -param pszSubscriptionAction [in]

URI of the event action.

### -param hr [in]

HRESULT indicating the nature of the error.

## -remarks

After an operation is subscribed to, the service proxy will attempt to automatically renew the subscription until the client calls the appropriate <b>Unsubscribe</b> method or until the subscription is ended by the service. When the renewal fails, <b>SubscriptionRenewalFailed</b> will be called to notify the client.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdeventingstatus">IWSDEventingStatus</a>