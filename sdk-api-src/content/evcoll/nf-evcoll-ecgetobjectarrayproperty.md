---
UID: NF:evcoll.EcGetObjectArrayProperty
title: EcGetObjectArrayProperty function (evcoll.h)
description: Retrieves property values for the event sources of a subscription.
helpviewer_keywords: ["EcGetObjectArrayProperty","EcGetObjectArrayProperty function","evcoll/EcGetObjectArrayProperty","wec.ecgetobjectarrayproperty","wes.ecgetobjectarrayproperty"]
old-location: wec\ecgetobjectarrayproperty.htm
tech.root: WEC
ms.assetid: a145c982-a1df-442f-8923-58f1db67ac25
ms.date: 12/05/2018
ms.keywords: EcGetObjectArrayProperty, EcGetObjectArrayProperty function, evcoll/EcGetObjectArrayProperty, wec.ecgetobjectarrayproperty, wes.ecgetobjectarrayproperty
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
 - EcGetObjectArrayProperty
 - evcoll/EcGetObjectArrayProperty
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
 - EcGetObjectArrayProperty
---

# EcGetObjectArrayProperty function


## -description

The <b>EcGetObjectArrayProperty</b> function retrieves  property values from a handle to an array of event source properties. The array contains property values for the event sources of a subscription.

## -parameters

### -param ObjectArray [in]

A handle to an array of properties for the event sources for a subscription. An  array handle that is returned by the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetsubscriptionproperty">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>PropertyId</i> parameter.

### -param PropertyId [in]

The property identifier for properties in the array. Specify a value from the <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_property_id">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. Get  the <b>Address</b>, <b>Enabled</b>, <b>UserName</b>, and <b>Password</b> properties in the array by specifying the <b>EcSubscriptionEventSourceAddress</b>, <b>EcSubscriptionEventSourceEnabled</b>, <b>EcSubscriptionEventSourceUserName</b>, or <b>EcSubscriptionEventSourcePassword</b> values.

### -param ArrayIndex [in]

The index of the array that specifies which event source to get the property from.

### -param Flags [in]

Reserved. Must be 0.

### -param PropertyValueBufferSize [in]

The size of the buffer that contains the value of the property. The size must be at least the size of an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EC_VARIANT</a> value.

### -param PropertyValueBuffer [in]

The user-supplied buffer to store property value into.

### -param PropertyValueBufferUsed [out]

The size of the user-supplied buffer that is used by the function on successful return, or the size that is necessary to store the property value when the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -returns

This function returns BOOL.

## -remarks

Arrays are zero-based, so the index for the first item in the array is 0.

The Password property for an event source or the subscription cannot be retrieved. For security reasons, an empty string is returned for the property value and the last error will be set to <b>ERROR_ACCESS_DENIED</b>.

A subscription can have multiple event sources, and each source can have an <b>Address</b>, <b>Enabled</b>, <b>UserName</b>, and <b>Password</b> property.


#### Examples

For example code using the <b>EcGetObjectArrayProperty</b> function, see <a href="/windows/desktop/WEC/displaying-the-properties-of-an-event-collector-subscription">Displaying the Properties of an Event Collector Subscription</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>