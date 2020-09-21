---
UID: NF:wmsdkidl.IWMReaderStreamClock.KillTimer
title: IWMReaderStreamClock::KillTimer (wmsdkidl.h)
description: The KillTimer method cancels a timer that has been set on the clock.
helpviewer_keywords: ["IWMReaderStreamClock interface [windows Media Format]","KillTimer method","IWMReaderStreamClock.KillTimer","IWMReaderStreamClock::KillTimer","IWMReaderStreamClockKillTimer","KillTimer","KillTimer method [windows Media Format]","KillTimer method [windows Media Format]","IWMReaderStreamClock interface","wmformat.iwmreaderstreamclock_killtimer","wmsdkidl/IWMReaderStreamClock::KillTimer"]
old-location: wmformat\iwmreaderstreamclock_killtimer.htm
tech.root: wmformat
ms.assetid: ebcd965f-8ea1-44e2-b1b4-c34a229058b2
ms.date: 12/05/2018
ms.keywords: IWMReaderStreamClock interface [windows Media Format],KillTimer method, IWMReaderStreamClock.KillTimer, IWMReaderStreamClock::KillTimer, IWMReaderStreamClockKillTimer, KillTimer, KillTimer method [windows Media Format], KillTimer method [windows Media Format],IWMReaderStreamClock interface, wmformat.iwmreaderstreamclock_killtimer, wmsdkidl/IWMReaderStreamClock::KillTimer
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderStreamClock::KillTimer
 - wmsdkidl/IWMReaderStreamClock::KillTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderStreamClock.KillTimer
---

# IWMReaderStreamClock::KillTimer


## -description

The <b>KillTimer</b> method cancels a timer that has been set on the clock.

## -parameters

### -param dwTimerId [in]

<b>DWORD</b> containing the timer identifier.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock">IWMReaderStreamClock Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderstreamclock-settimer">IWMReaderStreamClock::SetTimer</a>