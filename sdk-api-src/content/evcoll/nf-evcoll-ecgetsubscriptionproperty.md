---
UID: NF:evcoll.EcGetSubscriptionProperty
title: EcGetSubscriptionProperty function
author: windows-sdk-content
description: Retrieves a property value from a subscription object.
old-location: wec\ecgetsubscriptionproperty.htm
old-project: WEC
ms.assetid: 984d986d-1c59-4d0c-88f3-40c66ffe43dd
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcGetSubscriptionProperty, EcGetSubscriptionProperty function, evcoll/EcGetSubscriptionProperty, wec.ecgetsubscriptionproperty, wes.ecgetsubscriptionproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: EC_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wecapi.dll
api_name:
 - EcGetSubscriptionProperty
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcGetSubscriptionProperty function


## -description


The <b>EcGetSubscriptionProperty</b> function retrieves a specific property value from a subscription object. The subscription object is specified by the handle passed into the <i>Subscription</i> parameter.


## -parameters




### -param Subscription [in]

The handle to the subscription object.


### -param PropertyId [in]

An identifier that specifies which property of the subscription to get. Specify a value from the <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a> enumeration. If you specify the <b>EcSubscriptionEventSources</b> value, then a handle to an array (<a href="https://msdn.microsoft.com/b78bdaf8-e034-40fe-acf8-632313e4fd94">EC_OBJECT_ARRAY_PROPERTY_HANDLE</a>) will be returned. You can then use the <a href="https://msdn.microsoft.com/a145c982-a1df-442f-8923-58f1db67ac25">EcGetObjectArrayProperty</a> and <a href="https://msdn.microsoft.com/0c219e3b-a7dd-4a7f-8fb3-0d281351ba24">EcSetObjectArrayProperty</a>  functions to get and set the Address, Enabled, UserName, and Password properties in the array.


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




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

