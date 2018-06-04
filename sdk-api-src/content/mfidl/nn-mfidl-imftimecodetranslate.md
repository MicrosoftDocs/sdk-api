---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFTimecodeTranslate interface


## -description


Converts between Society of Motion Picture and Television Engineers (SMPTE) time codes and 100-nanosecond time units.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimecodeTranslate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimecodeTranslate</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/42b5de27-aaa6-4bd9-b2b0-3aeabfc28ef2">BeginConvertHNSToTimecode</a>
</td>
<td align="left" width="63%">
Starts an asynchronous call to convert time in 100-nanosecond units to SMPTE time code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e25d5e4-b4d7-4ca4-81c9-12c6d712322d">BeginConvertTimecodeToHNS</a>
</td>
<td align="left" width="63%">
Starts an asynchronous call to convert SMPTE time code to 100-nanosecond units.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9386748c-e551-49b8-89c3-65d721820736">EndConvertHNSToTimecode</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to convert time in 100-nanosecond units to SMPTE time code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b8b8ba-d03a-4a45-8788-38dbb2be8c6a">EndConvertTimecodeToHNS</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to convert time in SMPTE time code to 100-nanosecond units.

</td>
</tr>
</table> 


## -remarks



If an object supports this interface, it must expose the interface as a service. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier <b>MF_TIMECODE_SERVICE</b>.

The Advanced Streaming Format (ASF) media source exposes this interface.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/264a0e86-49e9-4777-956b-a83e9db52a25">Service Interfaces</a>
 

 

