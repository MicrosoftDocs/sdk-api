---
UID: NN:mfmediaengine.IMFMediaTimeRange
title: IMFMediaTimeRange
author: windows-sdk-content
description: Represents a list of time ranges, where each range is defined by a start and end time.
old-location: mf\imfmediatimerange.htm
tech.root: medfound
ms.assetid: E39646E6-66F4-4413-A84B-43039689AEE7
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFMediaTimeRange, IMFMediaTimeRange interface [Media Foundation], IMFMediaTimeRange interface [Media Foundation],described, mf.imfmediatimerange, mfmediaengine/IMFMediaTimeRange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfmediaengine.h
api_name:
 - IMFMediaTimeRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaTimeRange interface


## -description


Represents a list of time ranges, where each range is defined by a start and end time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaTimeRange</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaTimeRange</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaTimeRange</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6BA36A44-78AC-4868-9E6A-601C0740E67A">AddRange</a>
</td>
<td align="left" width="63%">
Adds a new range to the list of time ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F7CDC73E-CF14-48E2-9C8A-E1944099861A">Clear</a>
</td>
<td align="left" width="63%">
Clears the list of time ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67BA2464-D8F0-4A5C-9C12-DBD9AD0238A7">ContainsTime</a>
</td>
<td align="left" width="63%">
Queries whether a specified time falls within any of the time ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/864C0DEE-A1F7-488C-9A9D-366602667DE9">GetEnd</a>
</td>
<td align="left" width="63%">
Gets the end time for a specified time range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0865A667-A09E-4F42-A420-4A155AD34394">GetLength</a>
</td>
<td align="left" width="63%">
Gets the number of time ranges contained in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E02CFE99-78B8-4923-8922-467A55442802">GetStart</a>
</td>
<td align="left" width="63%">
Gets the start time for a specified time range.

</td>
</tr>
</table> 


## -remarks



The <b>IMFMediaTimeRange</b> interface corresponds to the <b>TimeRanges</b> interface in HTML5.

Several <a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a> methods return <b>IMFMediaTimeRange</b> pointers.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

