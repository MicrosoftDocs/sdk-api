---
UID: NF:tuner.IESRequestTunerEvent.GetEstimatedTime
title: IESRequestTunerEvent::GetEstimatedTime (tuner.h)
description: Gets a value indicating the amount of time that a device estimates it needs exclusive access to a tuner and its Conditional Access Services (CAS).
helpviewer_keywords: ["GetEstimatedTime","GetEstimatedTime method [Microsoft TV Technologies]","GetEstimatedTime method [Microsoft TV Technologies]","IESRequestTunerEvent interface","IESRequestTunerEvent interface [Microsoft TV Technologies]","GetEstimatedTime method","IESRequestTunerEvent.GetEstimatedTime","IESRequestTunerEvent::GetEstimatedTime","mstv.iesrequesttunerevent_getestimatedtime","tuner/IESRequestTunerEvent::GetEstimatedTime"]
old-location: mstv\iesrequesttunerevent_getestimatedtime.htm
tech.root: mstv
ms.assetid: 9968c1b1-5a4d-45a1-a083-afdbcc616f6d
ms.date: 12/05/2018
ms.keywords: GetEstimatedTime, GetEstimatedTime method [Microsoft TV Technologies], GetEstimatedTime method [Microsoft TV Technologies],IESRequestTunerEvent interface, IESRequestTunerEvent interface [Microsoft TV Technologies],GetEstimatedTime method, IESRequestTunerEvent.GetEstimatedTime, IESRequestTunerEvent::GetEstimatedTime, mstv.iesrequesttunerevent_getestimatedtime, tuner/IESRequestTunerEvent::GetEstimatedTime
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IESRequestTunerEvent::GetEstimatedTime
 - tuner/IESRequestTunerEvent::GetEstimatedTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESRequestTunerEvent.GetEstimatedTime
---

# IESRequestTunerEvent::GetEstimatedTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a value indicating the amount of time that a device estimates it  needs exclusive access to a tuner and its Conditional Access Services (CAS).

## -parameters

### -param pdwEstimatedTime [out, retval]

Gets the estimated time that exclusive access is needed, in seconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iesrequesttunerevent">IESRequestTunerEvent</a>