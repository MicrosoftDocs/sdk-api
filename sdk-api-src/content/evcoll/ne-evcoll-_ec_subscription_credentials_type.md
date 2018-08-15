---
UID: NE:evcoll._EC_SUBSCRIPTION_CREDENTIALS_TYPE
title: "_EC_SUBSCRIPTION_CREDENTIALS_TYPE"
author: windows-sdk-content
description: Specifies the type of credentials to use when communicating with event sources.
old-location: wec\ec_subscription_credentials_type.htm
old-project: WEC
ms.assetid: 5f2d3e26-1703-4afb-8b58-ee747bb156e3
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EC_SUBSCRIPTION_CREDENTIALS_TYPE, EC_SUBSCRIPTION_CREDENTIALS_TYPE enumeration, EcSubscriptionCredBasic, EcSubscriptionCredDefault, EcSubscriptionCredDigest, EcSubscriptionCredLocalMachine, EcSubscriptionCredNegotiate, _EC_SUBSCRIPTION_CREDENTIALS_TYPE, evcoll/EC_SUBSCRIPTION_CREDENTIALS_TYPE, evcoll/EcSubscriptionCredBasic, evcoll/EcSubscriptionCredDefault, evcoll/EcSubscriptionCredDigest, evcoll/EcSubscriptionCredLocalMachine, evcoll/EcSubscriptionCredNegotiate, wec.ec_subscription_credentials_type, wes.ec_subscription_credentials_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: evcoll.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EC_SUBSCRIPTION_CREDENTIALS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_CREDENTIALS_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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

