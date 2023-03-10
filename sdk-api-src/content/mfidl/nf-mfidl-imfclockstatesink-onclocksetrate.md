---
UID: NF:mfidl.IMFClockStateSink.OnClockSetRate
title: IMFClockStateSink::OnClockSetRate (mfidl.h)
description: Called when the rate changes on the presentation clock.
helpviewer_keywords: ["IMFClockStateSink interface [Media Foundation]","OnClockSetRate method","IMFClockStateSink.OnClockSetRate","IMFClockStateSink::OnClockSetRate","OnClockSetRate","OnClockSetRate method [Media Foundation]","OnClockSetRate method [Media Foundation]","IMFClockStateSink interface","ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998","mf.imfclockstatesink_onclocksetrate","mfidl/IMFClockStateSink::OnClockSetRate"]
old-location: mf\imfclockstatesink_onclocksetrate.htm
tech.root: mf
ms.assetid: ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998
ms.date: 12/05/2018
ms.keywords: IMFClockStateSink interface [Media Foundation],OnClockSetRate method, IMFClockStateSink.OnClockSetRate, IMFClockStateSink::OnClockSetRate, OnClockSetRate, OnClockSetRate method [Media Foundation], OnClockSetRate method [Media Foundation],IMFClockStateSink interface, ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998, mf.imfclockstatesink_onclocksetrate, mfidl/IMFClockStateSink::OnClockSetRate
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFClockStateSink::OnClockSetRate
 - mfidl/IMFClockStateSink::OnClockSetRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFClockStateSink.OnClockSetRate
---

# IMFClockStateSink::OnClockSetRate


## -description

Called when the rate changes on the presentation clock.

## -parameters

### -param hnsSystemTime [in]

The system time when the rate was set, in 100-nanosecond units.

### -param flRate [in]

The new rate, as a multiplier of the normal playback rate.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the presentation clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate">IMFRateControl::SetRate</a> method is called, the clock notifies the presentation time source by calling the time source's <b>OnClockSetRate</b> method. This call occurs synchronously within the <b>SetRate</b> method. If the time source returns an error from <b>OnClockSetRate</b>, the presentation clock's <b>SetRate</b> method returns an error and the state change does not take place.
      

For any object that is not the presentation time source, the <b>OnClockSetRate</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>