---
UID: NF:strmif.IAMClockAdjust.SetClockDelta
title: IAMClockAdjust::SetClockDelta (strmif.h)
author: windows-sdk-content
description: The SetClockDelta method adjusts the clock time.
old-location: dshow\iamclockadjust_setclockdelta.htm
tech.root: DirectShow
ms.assetid: f9bd4e69-343f-4150-ab12-b5ce405a3ac3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMClockAdjust interface [DirectShow],SetClockDelta method, IAMClockAdjust.SetClockDelta, IAMClockAdjust::SetClockDelta, IAMClockAdjustSetClockDelta, SetClockDelta, SetClockDelta method [DirectShow], SetClockDelta method [DirectShow],IAMClockAdjust interface, dshow.iamclockadjust_setclockdelta, strmif/IAMClockAdjust::SetClockDelta
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMClockAdjust.SetClockDelta
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMClockAdjust::SetClockDelta


## -description



The <code>SetClockDelta</code> method adjusts the clock time.




## -parameters




### -param rtDelta [in]

Specifies the amount by which to adjust the clock, as a <a href="https://msdn.microsoft.com/862c95bc-2e0a-42c0-b907-45f64f27bd41">REFERENCE_TIME</a> value. A positive value moves the clock forward, and a negative value moves the clock backward.


## -returns



Returns S_OK or an <b>HRESULT</b> error code.




## -remarks



The time values returned by <a href="https://msdn.microsoft.com/1fcf8b8a-f449-4f42-8061-cc4116867d9d">IReferenceClock::GetTime</a> are monotonically increasing. If you set the clock back, <b>GetTime</b> continues to report the old time until the internal clock catches up.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e24105a5-711a-498a-a07c-842307602613">IAMClockAdjust Interface</a>
 

 

