---
UID: NF:evcoll.EcGetObjectArraySize
title: EcGetObjectArraySize function
author: windows-sdk-content
description: Retrieves the number of indexes of the array of property values for the event sources of a subscription.
old-location: wec\ecgetobjectarraysize.htm
old-project: WEC
ms.assetid: f04c1748-d8b3-4000-a322-7854f8e7f5f9
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EcGetObjectArraySize, EcGetObjectArraySize function, evcoll/EcGetObjectArraySize, wec.ecgetobjectarraysize, wes.ecgetobjectarraysize
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
 - EcGetObjectArraySize
product: Windows
targetos: Windows
req.lib: Wecapi.lib
req.dll: Wecapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EcGetObjectArraySize function


## -description


The <b>EcGetObjectArraySize</b> function retrieves the size (the number of indexes) of the array of property values for the event sources of a subscription.


## -parameters




### -param ObjectArray [in]

A handle to the array from which to get the size. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="https://msdn.microsoft.com/984d986d-1c59-4d0c-88f3-40c66ffe43dd">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>PropertyId</i> parameter.


### -param ObjectArraySize [out]

The size of the array (the number of indexes).


## -returns



This function returns BOOL __stdcall.




## -remarks



Arrays are zero-based, so the index for the first item in the array is 0.


#### Examples

For example code using the <b>EcGetObjectArraySize</b> function, see <a href="https://msdn.microsoft.com/984e21cf-3671-4aca-9e8e-bcad1fa2f02c">Displaying the Properties of an Event Collector Subscription</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/48155df6-ba9c-4abe-ba84-6190cee95878">Windows Event Collector Functions</a>
 

 

