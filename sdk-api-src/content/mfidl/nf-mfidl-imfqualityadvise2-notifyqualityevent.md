---
UID: NF:mfidl.IMFQualityAdvise2.NotifyQualityEvent
title: IMFQualityAdvise2::NotifyQualityEvent (mfidl.h)
description: Forwards an MEQualityNotify event from the media sink.
helpviewer_keywords: ["IMFQualityAdvise2 interface [Media Foundation]","NotifyQualityEvent method","IMFQualityAdvise2.NotifyQualityEvent","IMFQualityAdvise2::NotifyQualityEvent","NotifyQualityEvent","NotifyQualityEvent method [Media Foundation]","NotifyQualityEvent method [Media Foundation]","IMFQualityAdvise2 interface","mf.imfqualityadvise2_notifyqualityevent","mfidl/IMFQualityAdvise2::NotifyQualityEvent"]
old-location: mf\imfqualityadvise2_notifyqualityevent.htm
tech.root: mf
ms.assetid: 7e39d421-1e7c-4b6d-beba-e24429271378
ms.date: 12/05/2018
ms.keywords: IMFQualityAdvise2 interface [Media Foundation],NotifyQualityEvent method, IMFQualityAdvise2.NotifyQualityEvent, IMFQualityAdvise2::NotifyQualityEvent, NotifyQualityEvent, NotifyQualityEvent method [Media Foundation], NotifyQualityEvent method [Media Foundation],IMFQualityAdvise2 interface, mf.imfqualityadvise2_notifyqualityevent, mfidl/IMFQualityAdvise2::NotifyQualityEvent
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFQualityAdvise2::NotifyQualityEvent
 - mfidl/IMFQualityAdvise2::NotifyQualityEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFQualityAdvise2.NotifyQualityEvent
---

# IMFQualityAdvise2::NotifyQualityEvent


## -description

Forwards an <a href="/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> event from the media sink.

## -parameters

### -param pEvent [in]

A pointer to the event's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface.

### -param pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_quality_advise_flags">MF_QUALITY_ADVISE_FLAGS</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2">IMFQualityAdvise2</a>