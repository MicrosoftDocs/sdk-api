---
UID: NF:evcoll.EcDeleteSubscription
title: EcDeleteSubscription function (evcoll.h)
description: Deletes an existing subscription.
helpviewer_keywords: ["EcDeleteSubscription","EcDeleteSubscription function","evcoll/EcDeleteSubscription","wec.ecdeletesubscription","wes.ecdeletesubscription"]
old-location: wec\ecdeletesubscription.htm
tech.root: WEC
ms.assetid: 301b982e-a7ab-47ef-99a7-bd63dded792b
ms.date: 12/05/2018
ms.keywords: EcDeleteSubscription, EcDeleteSubscription function, evcoll/EcDeleteSubscription, wec.ecdeletesubscription, wes.ecdeletesubscription
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
 - EcDeleteSubscription
 - evcoll/EcDeleteSubscription
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
 - EcDeleteSubscription
---

# EcDeleteSubscription function


## -description

The <b>EcDeleteSubscription</b> function deletes  an existing subscription that is specified by the <i>SubscriptionName</i> parameter. 

The function fails if the security descriptor of the subscription does not permit delete access for the calling process. 

If the subscription is active at the moment this API is called, then the subscription is deactivated.

## -parameters

### -param SubscriptionName [in]

The subscription to be deleted.

### -param Flags [in]

Reserved, must be 0.

## -returns

This function returns BOOL.

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>