---
UID: NN:mfmediaengine.IMFMediaTimeRange
title: IMFMediaTimeRange (mfmediaengine.h)
description: Represents a list of time ranges, where each range is defined by a start and end time.
helpviewer_keywords: ["IMFMediaTimeRange","IMFMediaTimeRange interface [Media Foundation]","IMFMediaTimeRange interface [Media Foundation]","described","mf.imfmediatimerange","mfmediaengine/IMFMediaTimeRange"]
old-location: mf\imfmediatimerange.htm
tech.root: medfound
ms.assetid: E39646E6-66F4-4413-A84B-43039689AEE7
ms.date: 12/05/2018
ms.keywords: IMFMediaTimeRange, IMFMediaTimeRange interface [Media Foundation], IMFMediaTimeRange interface [Media Foundation],described, mf.imfmediatimerange, mfmediaengine/IMFMediaTimeRange
f1_keywords:
- mfmediaengine/IMFMediaTimeRange
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaTimeRange interface


## -description


Represents a list of time ranges, where each range is defined by a start and end time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaTimeRange</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaTimeRange</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-addrange">AddRange</a>
</td>
<td align="left" width="63%">
Adds a new range to the list of time ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the list of time ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-containstime">ContainsTime</a>
</td>
<td align="left" width="63%">
Queries whether a specified time falls within any of the time ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-getend">GetEnd</a>
</td>
<td align="left" width="63%">
Gets the end time for a specified time range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the number of time ranges contained in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediatimerange-getstart">GetStart</a>
</td>
<td align="left" width="63%">
Gets the start time for a specified time range.

</td>
</tr>
</table> 


## -remarks



The <b>IMFMediaTimeRange</b> interface corresponds to the <b>TimeRanges</b> interface in HTML5.

Several <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a> methods return <b>IMFMediaTimeRange</b> pointers.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

