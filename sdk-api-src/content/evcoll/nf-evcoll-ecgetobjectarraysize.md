---
UID: NF:evcoll.EcGetObjectArraySize
title: EcGetObjectArraySize function (evcoll.h)
description: Retrieves the number of indexes of the array of property values for the event sources of a subscription.
helpviewer_keywords: ["EcGetObjectArraySize","EcGetObjectArraySize function","evcoll/EcGetObjectArraySize","wec.ecgetobjectarraysize","wes.ecgetobjectarraysize"]
old-location: wec\ecgetobjectarraysize.htm
tech.root: WEC
ms.assetid: f04c1748-d8b3-4000-a322-7854f8e7f5f9
ms.date: 12/05/2018
ms.keywords: EcGetObjectArraySize, EcGetObjectArraySize function, evcoll/EcGetObjectArraySize, wec.ecgetobjectarraysize, wes.ecgetobjectarraysize
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
 - EcGetObjectArraySize
 - evcoll/EcGetObjectArraySize
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
 - EcGetObjectArraySize
---

# EcGetObjectArraySize function


## -description

The <b>EcGetObjectArraySize</b> function retrieves the size (the number of indexes) of the array of property values for the event sources of a subscription.

## -parameters

### -param ObjectArray [in]

A handle to the array from which to get the size. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetsubscriptionproperty">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>PropertyId</i> parameter.

### -param ObjectArraySize [out]

The size of the array (the number of indexes).

## -returns

This function returns BOOL.

## -remarks

Arrays are zero-based, so the index for the first item in the array is 0.


#### Examples

For example code using the <b>EcGetObjectArraySize</b> function, see <a href="/windows/desktop/WEC/displaying-the-properties-of-an-event-collector-subscription">Displaying the Properties of an Event Collector Subscription</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>