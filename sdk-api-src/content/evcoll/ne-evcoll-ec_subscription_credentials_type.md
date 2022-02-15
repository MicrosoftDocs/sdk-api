---
UID: NE:evcoll._EC_SUBSCRIPTION_CREDENTIALS_TYPE
title: EC_SUBSCRIPTION_CREDENTIALS_TYPE (evcoll.h)
description: Specifies the type of credentials to use when communicating with event sources.
helpviewer_keywords: ["EC_SUBSCRIPTION_CREDENTIALS_TYPE","EC_SUBSCRIPTION_CREDENTIALS_TYPE enumeration","EcSubscriptionCredBasic","EcSubscriptionCredDefault","EcSubscriptionCredDigest","EcSubscriptionCredLocalMachine","EcSubscriptionCredNegotiate","evcoll/EC_SUBSCRIPTION_CREDENTIALS_TYPE","evcoll/EcSubscriptionCredBasic","evcoll/EcSubscriptionCredDefault","evcoll/EcSubscriptionCredDigest","evcoll/EcSubscriptionCredLocalMachine","evcoll/EcSubscriptionCredNegotiate","wec.ec_subscription_credentials_type","wes.ec_subscription_credentials_type"]
old-location: wec\ec_subscription_credentials_type.htm
tech.root: WEC
ms.assetid: 5f2d3e26-1703-4afb-8b58-ee747bb156e3
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_CREDENTIALS_TYPE, EC_SUBSCRIPTION_CREDENTIALS_TYPE enumeration, EcSubscriptionCredBasic, EcSubscriptionCredDefault, EcSubscriptionCredDigest, EcSubscriptionCredLocalMachine, EcSubscriptionCredNegotiate, evcoll/EC_SUBSCRIPTION_CREDENTIALS_TYPE, evcoll/EcSubscriptionCredBasic, evcoll/EcSubscriptionCredDefault, evcoll/EcSubscriptionCredDigest, evcoll/EcSubscriptionCredLocalMachine, evcoll/EcSubscriptionCredNegotiate, wec.ec_subscription_credentials_type, wes.ec_subscription_credentials_type
req.header: evcoll.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EC_SUBSCRIPTION_CREDENTIALS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_SUBSCRIPTION_CREDENTIALS_TYPE
 - evcoll/_EC_SUBSCRIPTION_CREDENTIALS_TYPE
 - EC_SUBSCRIPTION_CREDENTIALS_TYPE
 - evcoll/EC_SUBSCRIPTION_CREDENTIALS_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_CREDENTIALS_TYPE
---

# EC_SUBSCRIPTION_CREDENTIALS_TYPE enumeration


## -description

The <b>EC_SUBSCRIPTION_CREDENTIALS_TYPE</b> enumeration specifies the type of credentials to use when communicating with event sources.

## -enum-fields

### -field EcSubscriptionCredDefault:0

Negotiate with event sources to specify a proper authentication type without specifying a username and password for the subscription credentials.

### -field EcSubscriptionCredNegotiate

WinRM will negotiate with event sources to specify a proper authentication type for the subscription credentials.

### -field EcSubscriptionCredDigest

Use digest authentication for the subscription credentials.

### -field EcSubscriptionCredBasic

Send a username and password to use as credentials for the subscription.

### -field EcSubscriptionCredLocalMachine

Use the local computer's domain account credentials to create a subscription instead of using  user credentials for the subscription. This has the advantage of not having to manage user accounts and password expiration to simplify long lasting subscription management.

