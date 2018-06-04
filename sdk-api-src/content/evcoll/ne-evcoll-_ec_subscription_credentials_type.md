---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _EC_SUBSCRIPTION_CREDENTIALS_TYPE enumeration


## -description


The <b>EC_SUBSCRIPTION_CREDENTIALS_TYPE</b> enumeration specifies the type of credentials to use when communicating with event sources.


## -enum-fields




### -field EcSubscriptionCredDefault

Negotiate with event sources to specify a proper authentication type without specifying a username and password for the subscription credentials.


### -field EcSubscriptionCredNegotiate

WinRM will negotiate with event sources to specify a proper authentication type for the subscription credentials.


### -field EcSubscriptionCredDigest

Use digest authentication for the subscription credentials.


### -field EcSubscriptionCredBasic

Send a username and password to use as credentials for the subscription.


### -field EcSubscriptionCredLocalMachine

Use the local computer's domain account credentials to create a subscription instead of using  user credentials for the subscription. This has the advantage of not having to manage user accounts and password expiration to simplify long lasting subscription management.

