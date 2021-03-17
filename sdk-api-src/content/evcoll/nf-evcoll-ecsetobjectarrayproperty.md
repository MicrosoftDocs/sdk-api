---
UID: NF:evcoll.EcSetObjectArrayProperty
title: EcSetObjectArrayProperty function (evcoll.h)
description: Sets a property value in an array of property values for the event sources of a subscription.
helpviewer_keywords: ["EcSetObjectArrayProperty","EcSetObjectArrayProperty function","evcoll/EcSetObjectArrayProperty","wec.ecsetobjectarrayproperty","wes.ecsetobjectarrayproperty"]
old-location: wec\ecsetobjectarrayproperty.htm
tech.root: WEC
ms.assetid: 0c219e3b-a7dd-4a7f-8fb3-0d281351ba24
ms.date: 12/05/2018
ms.keywords: EcSetObjectArrayProperty, EcSetObjectArrayProperty function, evcoll/EcSetObjectArrayProperty, wec.ecsetobjectarrayproperty, wes.ecsetobjectarrayproperty
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
 - EcSetObjectArrayProperty
 - evcoll/EcSetObjectArrayProperty
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
 - EcSetObjectArrayProperty
---

# EcSetObjectArrayProperty function


## -description

The <b>EcSetObjectArrayProperty</b> function sets a property value in an array of property values for the event sources of a subscription.

## -parameters

### -param ObjectArray [in]

A handle to the array that contains the property value to set. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetsubscriptionproperty">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.

### -param PropertyId [in]

An identifier that specifies which property to set. Specify a value from the <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_property_id">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. Set  the Address, Enabled, UserName, and Password properties in the array by specifying the <b>EcSubscriptionEventSourceAddress</b>, <b>EcSubscriptionEventSourceEnabled</b>, <b>EcSubscriptionEventSourceUserName</b>, or <b>EcSubscriptionEventSourcePassword</b> values.

### -param ArrayIndex [in]

The index of the  object in the array to set a property value on.

### -param Flags [in]

Reserved. Must be 0.

### -param PropertyValue [in]

The value of the property.

## -returns

This function returns BOOL.

## -remarks

Arrays are zero-based, so the index for the first item in the array is 0.


#### Examples

For example code using the <b>EcSetObjectArrayProperty</b> function, see <a href="/windows/desktop/WEC/adding-an-event-source-to-an-event-collector-subscription">Adding an Event Source to a Collector Initiated Subscription</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>