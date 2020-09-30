---
UID: NF:evcoll.EcGetSubscriptionProperty
title: EcGetSubscriptionProperty function (evcoll.h)
description: Retrieves a property value from a subscription object.
helpviewer_keywords: ["EcGetSubscriptionProperty","EcGetSubscriptionProperty function","evcoll/EcGetSubscriptionProperty","wec.ecgetsubscriptionproperty","wes.ecgetsubscriptionproperty"]
old-location: wec\ecgetsubscriptionproperty.htm
tech.root: WEC
ms.assetid: 984d986d-1c59-4d0c-88f3-40c66ffe43dd
ms.date: 12/05/2018
ms.keywords: EcGetSubscriptionProperty, EcGetSubscriptionProperty function, evcoll/EcGetSubscriptionProperty, wec.ecgetsubscriptionproperty, wes.ecgetsubscriptionproperty
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
 - EcGetSubscriptionProperty
 - evcoll/EcGetSubscriptionProperty
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
 - EcGetSubscriptionProperty
---

# EcGetSubscriptionProperty function


## -description

The <b>EcGetSubscriptionProperty</b> function retrieves a specific property value from a subscription object. The subscription object is specified by the handle passed into the <i>Subscription</i> parameter.

## -parameters

### -param Subscription [in]

The handle to the subscription object.

### -param PropertyId [in]

An identifier that specifies which property of the subscription to get. Specify a value from the <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_property_id">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. If you specify the <b>EcSubscriptionEventSources</b> value, then a handle to an array (<a href="/windows/desktop/WEC/windows-event-collector-data-types">EC_OBJECT_ARRAY_PROPERTY_HANDLE</a>) will be returned. You can then use the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetobjectarrayproperty">EcGetObjectArrayProperty</a> and <a href="/windows/desktop/api/evcoll/nf-evcoll-ecsetobjectarrayproperty">EcSetObjectArrayProperty</a>  functions to get and set the Address, Enabled, UserName, and Password properties in the array.

### -param Flags [in]

Reserved. Must be <b>NULL</b>.

### -param PropertyValueBufferSize [in]

The size of the user-supplied buffer to store the property value into.

### -param PropertyValueBuffer [in]

The user-supplied buffer to store property value into.

### -param PropertyValueBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the property value when function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -returns

This function returns BOOL.

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>