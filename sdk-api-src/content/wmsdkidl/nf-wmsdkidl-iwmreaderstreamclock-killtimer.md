---
UID: NF:wmsdkidl.IWMReaderStreamClock.KillTimer
title: IWMReaderStreamClock::KillTimer
author: windows-sdk-content
description: The KillTimer method cancels a timer that has been set on the clock.
old-location: wmformat\iwmreaderstreamclock_killtimer.htm
tech.root: wmformat
ms.assetid: ebcd965f-8ea1-44e2-b1b4-c34a229058b2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderStreamClock interface [windows Media Format],KillTimer method, IWMReaderStreamClock.KillTimer, IWMReaderStreamClock::KillTimer, IWMReaderStreamClockKillTimer, KillTimer, KillTimer method [windows Media Format], KillTimer method [windows Media Format],IWMReaderStreamClock interface, wmformat.iwmreaderstreamclock_killtimer, wmsdkidl/IWMReaderStreamClock::KillTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/0f170b6d-fd93-4bf8-8a98-f2a80f03b380">IWMReaderStreamClock Interface</a>



<a href="https://msdn.microsoft.com/15d991e0-a271-4427-844f-5e4a9bbc6507">IWMReaderStreamClock::SetTimer</a>
 

 

