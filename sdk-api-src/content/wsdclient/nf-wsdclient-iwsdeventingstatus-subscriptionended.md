---
UID: NF:wsdclient.IWSDEventingStatus.SubscriptionEnded
title: IWSDEventingStatus::SubscriptionEnded (wsdclient.h)
author: windows-sdk-content
description: Called when the device terminated the subscription.
old-location: ncd\iwsdeventingstatus_subscriptionended.htm
tech.root: WsdApi
ms.assetid: 4ccb16ed-d7c6-4242-ae53-9e58cecc475b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDEventingStatus interface,SubscriptionEnded method, IWSDEventingStatus.SubscriptionEnded, IWSDEventingStatus::SubscriptionEnded, SubscriptionEnded, SubscriptionEnded method, SubscriptionEnded method,IWSDEventingStatus interface, ncd.iwsdeventingstatus_subscriptionended, wsdclient/IWSDEventingStatus::SubscriptionEnded
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
 - IWSDEventingStatus.SubscriptionEnded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEventingStatus::SubscriptionEnded


## -description


Called when the device terminated the subscription.


## -parameters




### -param pszSubscriptionAction [in]

URI of the event action.


## -returns



This method does not return a value.




## -remarks



After an operation is subscribed to, the service proxy will listen for SubscriptionEnd messages from the subscription manager. If one is received for a specified subscription, <b>SubscriptionEnded</b> will be called to notify the client. <b>SubscriptionEnded</b> will not be called if the service proxy unsubscribes from the operation or if the host service goes offline.




## -see-also




<a href="https://msdn.microsoft.com/04e6ea03-f9b5-48d9-940f-532bb3a85ff0">IWSDEventingStatus</a>
 

 

