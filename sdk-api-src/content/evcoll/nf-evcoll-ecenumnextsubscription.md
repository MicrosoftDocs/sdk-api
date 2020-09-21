---
UID: NF:evcoll.EcEnumNextSubscription
title: EcEnumNextSubscription function (evcoll.h)
description: Continues the enumeration of the subscriptions registered on the local machine.
helpviewer_keywords: ["EcEnumNextSubscription","EcEnumNextSubscription function","evcoll/EcEnumNextSubscription","wec.ecenumnextsubscription","wes.ecenumnextsubscription"]
old-location: wec\ecenumnextsubscription.htm
tech.root: WEC
ms.assetid: 4228c9ca-6143-4301-8ff3-0ee296a53239
ms.date: 12/05/2018
ms.keywords: EcEnumNextSubscription, EcEnumNextSubscription function, evcoll/EcEnumNextSubscription, wec.ecenumnextsubscription, wes.ecenumnextsubscription
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
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EcEnumNextSubscription
 - evcoll/EcEnumNextSubscription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcEnumNextSubscription
---

# EcEnumNextSubscription function


## -description

The <b>EcEnumNextSubscription</b> function continues the enumeration of the subscriptions registered on the local machine.

## -parameters

### -param SubscriptionEnum [in]

The handle to the enumerator object that is returned from the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecopensubscriptionenum">EcOpenSubscriptionEnum</a> function.

### -param SubscriptionNameBufferSize [in]

The size of the user-supplied buffer (in chars) to store the subscription name.

### -param SubscriptionNameBuffer [in]

The user-supplied buffer to store the subscription name.

### -param SubscriptionNameBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the subscription name when the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -returns

This function returns BOOL.

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>