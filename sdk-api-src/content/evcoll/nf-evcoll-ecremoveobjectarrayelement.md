---
UID: NF:evcoll.EcRemoveObjectArrayElement
title: EcRemoveObjectArrayElement function (evcoll.h)
description: Removes an element from an array of objects that contain property values for the event sources of a subscription.
helpviewer_keywords: ["EcRemoveObjectArrayElement","EcRemoveObjectArrayElement function","evcoll/EcRemoveObjectArrayElement","wec.ecremoveobjectarrayelement","wes.ecremoveobjectarrayelement"]
old-location: wec\ecremoveobjectarrayelement.htm
tech.root: WEC
ms.assetid: 6c76ca94-b7bc-4590-be0b-6d6f499dda5a
ms.date: 12/05/2018
ms.keywords: EcRemoveObjectArrayElement, EcRemoveObjectArrayElement function, evcoll/EcRemoveObjectArrayElement, wec.ecremoveobjectarrayelement, wes.ecremoveobjectarrayelement
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
 - EcRemoveObjectArrayElement
 - evcoll/EcRemoveObjectArrayElement
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
 - EcRemoveObjectArrayElement
---

# EcRemoveObjectArrayElement function


## -description

The <b>EcRemoveObjectArrayElement</b> function removes an element from an array of objects that contain property values for the event sources of a subscription.

## -parameters

### -param ObjectArray [in]

A  handle to the array in which to remove the element. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetsubscriptionproperty">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.

### -param ArrayIndex [in]

The index of the element to remove from the array.

## -returns

This function returns BOOL.

## -remarks

Arrays are zero-based, so the index for the first item in the array is 0.


#### Examples

For example code using the <b>EcRemoveObjectArrayElement</b> function, see <a href="/windows/desktop/WEC/removing-an-event-source-from-an-event-collector-subscription">Removing an Event Source from a Collector Initiated Subscription</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>