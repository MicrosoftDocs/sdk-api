---
UID: NF:strmif.IAMTuner.RegisterNotificationCallBack
title: IAMTuner::RegisterNotificationCallBack (strmif.h)
description: The RegisterNotificationCallBack method enables an object to receive event notifications when the tuner changes state.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","RegisterNotificationCallBack method","IAMTuner.RegisterNotificationCallBack","IAMTuner::RegisterNotificationCallBack","IAMTunerRegisterNotificationCallBack","RegisterNotificationCallBack","RegisterNotificationCallBack method [DirectShow]","RegisterNotificationCallBack method [DirectShow]","IAMTuner interface","dshow.iamtuner_registernotificationcallback","strmif/IAMTuner::RegisterNotificationCallBack"]
old-location: dshow\iamtuner_registernotificationcallback.htm
tech.root: dshow
ms.assetid: e169039f-bce7-495a-a40f-385fa3d3d2ab
ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],RegisterNotificationCallBack method, IAMTuner.RegisterNotificationCallBack, IAMTuner::RegisterNotificationCallBack, IAMTunerRegisterNotificationCallBack, RegisterNotificationCallBack, RegisterNotificationCallBack method [DirectShow], RegisterNotificationCallBack method [DirectShow],IAMTuner interface, dshow.iamtuner_registernotificationcallback, strmif/IAMTuner::RegisterNotificationCallBack
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTuner::RegisterNotificationCallBack
 - strmif/IAMTuner::RegisterNotificationCallBack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.RegisterNotificationCallBack
---

# IAMTuner::RegisterNotificationCallBack


## -description

The <code>RegisterNotificationCallBack</code> method enables an object to receive event notifications when the tuner changes state.



This method is not implemented.

## -parameters

### -param pNotify [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification</a> interface that will receive the event notifications.

### -param lEvents [in]

Flag indicating that an event has occurred.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>