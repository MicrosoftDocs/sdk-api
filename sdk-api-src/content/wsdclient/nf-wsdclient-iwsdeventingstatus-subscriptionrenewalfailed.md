---
UID: NF:wsdclient.IWSDEventingStatus.SubscriptionRenewalFailed
title: IWSDEventingStatus::SubscriptionRenewalFailed
author: windows-sdk-content
description: Called when the subscription for the specified event action could not be renewed.
old-location: ncd\iwsdeventingstatus_subscriptionrenewalfailed.htm
old-project: WsdApi
ms.assetid: d76bb6ae-bb4d-4226-be0d-4fd37b0212a9
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDEventingStatus interface,SubscriptionRenewalFailed method, IWSDEventingStatus.SubscriptionRenewalFailed, IWSDEventingStatus::SubscriptionRenewalFailed, SubscriptionRenewalFailed, SubscriptionRenewalFailed method, SubscriptionRenewalFailed method,IWSDEventingStatus interface, ncd.iwsdeventingstatus_subscriptionrenewalfailed, wsdclient/IWSDEventingStatus::SubscriptionRenewalFailed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDEventingStatus.SubscriptionRenewalFailed
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDEventingStatus::SubscriptionRenewalFailed


## -description


Called when the subscription for the specified event action could not be renewed.


## -parameters




### -param pszSubscriptionAction [in]

URI of the event action.


### -param hr [in]

HRESULT indicating the nature of the error.


## -returns



This method does not return a value.




## -remarks



After an operation is subscribed to, the service proxy will attempt to automatically renew the subscription until the client calls the appropriate <b>Unsubscribe</b> method or until the subscription is ended by the service. When the renewal fails, <b>SubscriptionRenewalFailed</b> will be called to notify the client.




## -see-also




<a href="https://msdn.microsoft.com/04e6ea03-f9b5-48d9-940f-532bb3a85ff0">IWSDEventingStatus</a>
 

 

