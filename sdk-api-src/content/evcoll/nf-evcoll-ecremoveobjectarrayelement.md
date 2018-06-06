---
UID: NF:evcoll.EcRemoveObjectArrayElement
title: EcRemoveObjectArrayElement function
author: windows-sdk-content
description: Removes an element from an array of objects that contain property values for the event sources of a subscription.
old-location: wec\ecremoveobjectarrayelement.htm
old-project: WEC
ms.assetid: 6c76ca94-b7bc-4590-be0b-6d6f499dda5a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcRemoveObjectArrayElement, EcRemoveObjectArrayElement function, evcoll/EcRemoveObjectArrayElement, wec.ecremoveobjectarrayelement, wes.ecremoveobjectarrayelement
ms.prod: windows
ms.technology: windows-sdk
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
 - EcRemoveObjectArrayElement
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcRemoveObjectArrayElement function


## -description


The <b>EcRemoveObjectArrayElement</b> function removes an element from an array of objects that contain property values for the event sources of a subscription.


## -parameters




### -param ObjectArray [in]

A  handle to the array in which to remove the element. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="https://msdn.microsoft.com/984d986d-1c59-4d0c-88f3-40c66ffe43dd">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.


### -param ArrayIndex [in]

The index of the element to remove from the array.


## -returns



This function returns BOOL.




## -remarks



Arrays are zero-based, so the index for the first item in the array is 0.


#### Examples

For example code using the <b>EcRemoveObjectArrayElement</b> function, see <a href="https://msdn.microsoft.com/6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b">Removing an Event Source from a Collector Initiated Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

