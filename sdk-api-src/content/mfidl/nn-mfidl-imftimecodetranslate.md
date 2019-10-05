---
UID: NN:mfidl.IMFTimecodeTranslate
title: IMFTimecodeTranslate (mfidl.h)
author: windows-sdk-content
description: Converts between Society of Motion Picture and Television Engineers (SMPTE) time codes and 100-nanosecond time units.
old-location: mf\imftimecodetranslate.htm
tech.root: medfound
ms.assetid: 935ec6b3-12e6-4458-b8a1-ffeb4159d957
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTimecodeTranslate, IMFTimecodeTranslate interface [Media Foundation], IMFTimecodeTranslate interface [Media Foundation],described, mf.imftimecodetranslate, mfidl/IMFTimecodeTranslate
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFTimecodeTranslate"
dev_langs:
 - c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFTimecodeTranslate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimecodeTranslate interface


## -description


Converts between Society of Motion Picture and Television Engineers (SMPTE) time codes and 100-nanosecond time units.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimecodeTranslate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimecodeTranslate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimecodeTranslate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverthnstotimecode">BeginConvertHNSToTimecode</a>
</td>
<td align="left" width="63%">
Starts an asynchronous call to convert time in 100-nanosecond units to SMPTE time code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-beginconverttimecodetohns">BeginConvertTimecodeToHNS</a>
</td>
<td align="left" width="63%">
Starts an asynchronous call to convert SMPTE time code to 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverthnstotimecode">EndConvertHNSToTimecode</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to convert time in 100-nanosecond units to SMPTE time code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftimecodetranslate-endconverttimecodetohns">EndConvertTimecodeToHNS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to convert time in SMPTE time code to 100-nanosecond units.

</td>
</tr>
</table> 


## -remarks



If an object supports this interface, it must expose the interface as a service. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier <b>MF_TIMECODE_SERVICE</b>.

The Advanced Streaming Format (ASF) media source exposes this interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
 

 

