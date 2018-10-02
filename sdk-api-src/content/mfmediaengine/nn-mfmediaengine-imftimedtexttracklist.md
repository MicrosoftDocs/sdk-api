---
UID: NN:mfmediaengine.IMFTimedTextTrackList
title: IMFTimedTextTrackList
author: windows-sdk-content
description: Represents a list of timed-text tracks.
old-location: mf\imftimedtexttracklist.htm
tech.root: MedFound
ms.assetid: EA94A81E-3B1D-4723-B00F-B216991E19E5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IMFTimedTextTrackList, IMFTimedTextTrackList interface [Media Foundation], IMFTimedTextTrackList interface [Media Foundation],described, mf.imftimedtexttracklist, mfmediaengine/IMFTimedTextTrackList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFTimedTextTrackList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextTrackList interface


## -description


Represents a list of timed-text tracks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTimedTextTrackList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTimedTextTrackList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTimedTextTrackList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/468BF969-9D8D-4866-8E33-F1CC6F09E90A">GetLength</a>
</td>
<td align="left" width="63%">
Gets the length, in tracks, of the timed-text-track list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5AF4F317-E46D-459A-900B-6D4796CD59A2">GetTrack</a>
</td>
<td align="left" width="63%">
Gets a text track in the list from the index of the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5653ED8A-36B1-488C-9D76-50D64BA78BA8">GetTrackById</a>
</td>
<td align="left" width="63%">
Gets a text track in the list from the identifier of the track.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

