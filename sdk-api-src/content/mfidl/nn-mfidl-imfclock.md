---
UID: NN:mfidl.IMFClock
title: IMFClock (mfidl.h)

description: Provides timing information from a clock in Microsoft Media Foundation.
old-location: mf\imfclock.htm
tech.root: medfound
ms.assetid: 3a60bfec-8511-4a84-a833-e0c73c593970

ms.date: 12/05/2018
ms.keywords: 3a60bfec-8511-4a84-a833-e0c73c593970, IMFClock, IMFClock interface [Media Foundation], IMFClock interface [Media Foundation],described, mf.imfclock, mfidl/IMFClock
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFClock"
dev_langs:
 - c++
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
 - IMFClock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFClock interface


## -description


Provides timing information from a clock in Microsoft Media Foundation.

Clocks and some media sinks expose this interface through <b>QueryInterface</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFClock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFClock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFClock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getclockcharacteristics">GetClockCharacteristics</a>
</td>
<td align="left" width="63%">
Retrieves the characteristics of the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcontinuitykey">GetContinuityKey</a>
</td>
<td align="left" width="63%">
Retrieves the clock's continuity key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime">GetCorrelatedTime</a>
</td>
<td align="left" width="63%">
Retrieves the last clock time that was correlated with system time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of the clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfclock-getstate">GetState</a>
</td>
<td align="left" width="63%">
Retrieves the current state of the clock.

</td>
</tr>
</table> 


## -remarks



The <b>IMFClock</b> interface applies to any kind of clock. The presentation clock exposes the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface in addition to <b>IMFClock</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
 

 

