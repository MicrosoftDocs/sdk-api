---
UID: NF:evcoll.EcSetObjectArrayProperty
title: EcSetObjectArrayProperty function
author: windows-driver-content
description: Sets a property value in an array of property values for the event sources of a subscription.
old-location: wec\ecsetobjectarrayproperty.htm
old-project: WEC
ms.assetid: 0c219e3b-a7dd-4a7f-8fb3-0d281351ba24
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EcSetObjectArrayProperty, EcSetObjectArrayProperty function, evcoll/EcSetObjectArrayProperty, wec.ecsetobjectarrayproperty, wes.ecsetobjectarrayproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: EC_VARIANT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wecapi.dll
api_name:
-	EcSetObjectArrayProperty
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcSetObjectArrayProperty function


## -description


The <b>EcSetObjectArrayProperty</b> function sets a property value in an array of property values for the event sources of a subscription.


## -parameters




### -param ObjectArray [in]

A handle to the array that contains the property value to set. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="https://msdn.microsoft.com/984d986d-1c59-4d0c-88f3-40c66ffe43dd">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.


### -param PropertyId [in]

An identifier that specifies which property to set. Specify a value from the <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. Set  the Address, Enabled, UserName, and Password properties in the array by specifying the <b>EcSubscriptionEventSourceAddress</b>, <b>EcSubscriptionEventSourceEnabled</b>, <b>EcSubscriptionEventSourceUserName</b>, or <b>EcSubscriptionEventSourcePassword</b> values.


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

For example code using the <b>EcSetObjectArrayProperty</b> function, see <a href="https://msdn.microsoft.com/f0100938-1702-4ef7-b20e-a0e8df224d18">Adding an Event Source to a Collector Initiated Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

