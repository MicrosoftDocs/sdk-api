---
UID: NF:evcoll.EcInsertObjectArrayElement
title: EcInsertObjectArrayElement function (evcoll.h)
description: Inserts an empty object into an array of property values for the event sources of a subscription.
helpviewer_keywords: ["EcInsertObjectArrayElement","EcInsertObjectArrayElement function","evcoll/EcInsertObjectArrayElement","wec.ecinsertobjectarrayelement","wes.ecinsertobjectarrayelement"]
old-location: wec\ecinsertobjectarrayelement.htm
tech.root: WEC
ms.assetid: 65b0db2f-f929-4d7e-8804-c93b9e127323
ms.date: 12/05/2018
ms.keywords: EcInsertObjectArrayElement, EcInsertObjectArrayElement function, evcoll/EcInsertObjectArrayElement, wec.ecinsertobjectarrayelement, wes.ecinsertobjectarrayelement
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
 - EcInsertObjectArrayElement
 - evcoll/EcInsertObjectArrayElement
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
 - EcInsertObjectArrayElement
---

# EcInsertObjectArrayElement function


## -description

The <b>EcInsertObjectArrayElement</b> function inserts an empty object into an array of property values for the event sources of a subscription. The object is inserted at a specified array index.

## -parameters

### -param ObjectArray [in]

A  handle to the array in which the object is inserted into. The array contains property values for the event sources of a subscription. The array handle is returned by the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecgetsubscriptionproperty">EcGetSubscriptionProperty</a> method when the <b>EcSubscriptionEventSources</b> value is passed into the <i>Subscription</i> parameter.

### -param ArrayIndex [in]

An array index indicating where to insert the object.

## -returns

This function returns BOOL.

## -remarks

Arrays are zero-based, so the index for the first item in the array is 0.

Use the <a href="/windows/desktop/api/evcoll/nf-evcoll-ecsetobjectarrayproperty">EcSetObjectArrayProperty</a> to set individual properties of an empty object inserted into the array specified in the <i>ObjectArray</i> parameter.


#### Examples

For example code using the <b>EcInsertObjectArrayElement</b> function, see <a href="/windows/desktop/WEC/adding-an-event-source-to-an-event-collector-subscription">Adding an Event Source to a Collector Initiated Subscription</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/WEC/windows-event-collector-functions">Windows Event Collector Functions</a>