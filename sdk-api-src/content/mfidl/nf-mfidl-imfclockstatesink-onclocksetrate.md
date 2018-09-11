---
UID: NF:mfidl.IMFClockStateSink.OnClockSetRate
title: IMFClockStateSink::OnClockSetRate
author: windows-sdk-content
description: Called when the rate changes on the presentation clock.
old-location: mf\imfclockstatesink_onclocksetrate.htm
tech.root: medfound
ms.assetid: ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFClockStateSink interface [Media Foundation],OnClockSetRate method, IMFClockStateSink.OnClockSetRate, IMFClockStateSink::OnClockSetRate, OnClockSetRate, OnClockSetRate method [Media Foundation], OnClockSetRate method [Media Foundation],IMFClockStateSink interface, ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998, mf.imfclockstatesink_onclocksetrate, mfidl/IMFClockStateSink::OnClockSetRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the presentation clock's <a href="https://msdn.microsoft.com/428d73fa-f284-4861-a41e-04ea7709db0f">IMFRateControl::SetRate</a> method is called, the clock notifies the presentation time source by calling the time source's <b>OnClockSetRate</b> method. This call occurs synchronously within the <b>SetRate</b> method. If the time source returns an error from <b>OnClockSetRate</b>, the presentation clock's <b>SetRate</b> method returns an error and the state change does not take place.
      

For any object that is not the presentation time source, the <b>OnClockSetRate</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.
      




## -see-also




<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

