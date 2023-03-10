---
UID: NF:evcoll.EcOpenSubscription
title: EcOpenSubscription function (evcoll.h)
description: Opens an existing subscription or creates a new subscription.
helpviewer_keywords: ["EcOpenSubscription","EcOpenSubscription function","evcoll/EcOpenSubscription","wec.ecopensubscription","wes.ecopensubscription"]
old-location: wec\ecopensubscription.htm
tech.root: WEC
ms.assetid: 3b4ef765-b557-4142-ba7d-e2556bd067ec
ms.date: 12/05/2018
ms.keywords: EcOpenSubscription, EcOpenSubscription function, evcoll/EcOpenSubscription, wec.ecopensubscription, wes.ecopensubscription
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
 - EcOpenSubscription
 - evcoll/EcOpenSubscription
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
 - EcOpenSubscription
---

# EcOpenSubscription function


## -description

The <b>EcOpenSubscription</b> function is used to open an existing subscription or create a new subscription according to the flag value specified.

## -parameters

### -param SubscriptionName [in]

Specifies the name of the subscription. The value provided for this parameter should be unique within the computer's scope.

### -param AccessMask [in]

An access mask that specifies the desired access rights to the subscription. Use the <a href="/windows/desktop/WEC/windows-event-collector-constants">EC_READ_ACCESS</a> or <a href="/windows/desktop/WEC/windows-event-collector-constants">EC_WRITE_ACCESS</a> constants to specify the access rights. The function fails if the security descriptor of the subscription does not permit the requested access for the calling process.

### -param Flags [in]

A value specifying whether a new or existing subscription will be opened. Use the <b>EC_CREATE_NEW</b>, <b>EC_OPEN_ALWAYS</b>, or <b>EC_OPEN_EXISTING</b> constants.

## -returns

If the function succeeds, it returns a handle (<a href="/windows/desktop/WEC/windows-event-collector-data-types">EC_HANDLE</a>) to a new subscription object. Returns <b>NULL</b> otherwise, in which case use the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to obtain the error code.

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>