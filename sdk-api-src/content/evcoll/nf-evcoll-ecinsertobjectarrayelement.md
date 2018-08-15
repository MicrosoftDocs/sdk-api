---
UID: NF:evcoll.EcInsertObjectArrayElement
title: EcInsertObjectArrayElement function
author: windows-sdk-content
description: Inserts an empty object into an array of property values for the event sources of a subscription.
old-location: wec\ecinsertobjectarrayelement.htm
old-project: WEC
ms.assetid: 65b0db2f-f929-4d7e-8804-c93b9e127323
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcInsertObjectArrayElement, EcInsertObjectArrayElement function, evcoll/EcInsertObjectArrayElement, wec.ecinsertobjectarrayelement, wes.ecinsertobjectarrayelement
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
 - EcInsertObjectArrayElement
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcInsertObjectArrayElement function


## -description


The <b>EcInsertObjectArrayElement</b> function inserts an empty object into an array of property values for the event sources of a subscription. The object is inserted at a specified array index.


## -parameters




### -param ObjectArray [in]

A  handle to the array in which the object is inserted into. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="https://msdn.microsoft.com/984d986d-1c59-4d0c-88f3-40c66ffe43dd">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.


### -param ArrayIndex [in]

An array index indicating where to insert the object.


## -returns



This function returns BOOL.




## -remarks



Arrays are zero-based, so the index for the first item in the array is 0.

Use the <a href="https://msdn.microsoft.com/0c219e3b-a7dd-4a7f-8fb3-0d281351ba24">EcSetObjectArrayProperty</a> to set individual properties of an empty object inserted into the array specified in the <i>ObjectArray</i> parameter.


#### Examples

For example code using the <b>EcInsertObjectArrayElement</b> function, see <a href="https://msdn.microsoft.com/f0100938-1702-4ef7-b20e-a0e8df224d18">Adding an Event Source to a Collector Initiated Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

