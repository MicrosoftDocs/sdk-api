---
UID: NN:strmif.IDDrawExclModeVideoCallback
title: IDDrawExclModeVideoCallback
author: windows-sdk-content
description: The IDDrawExclModeVideoCallback interface is a callback interface for the IDDrawExclModeVideo interface.This callback interface enables applications to get synchronous notification about changes to the overlay position, size, visibility, and so on, so that the application can adjust its video visibility, size, and position. This avoids any color key flash at the beginning, end, or during playback. The application must implement the interface. It is important that none of the methods block or slow down the video processing, because this will cause problems with playback.Use this interface if you are writing a filter that supports IDDrawExclModeVideo or needs to generate callbacks to enable an application to draw color keys at the right time.
old-location: dshow\iddrawexclmodevideocallback.htm
tech.root: DirectShow
ms.assetid: 7f22d4cd-93e0-4d7d-b8f3-932488d2c672
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDDrawExclModeVideoCallback, IDDrawExclModeVideoCallback interface [DirectShow], IDDrawExclModeVideoCallback interface [DirectShow],described, IDDrawExclModeVideoCallbackInterface, dshow.iddrawexclmodevideocallback, strmif/IDDrawExclModeVideoCallback
ms.topic: interface
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
 - IDDrawExclModeVideoCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDDrawExclModeVideoCallback interface


## -description



The <code>IDDrawExclModeVideoCallback</code> interface is a callback interface for the <a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo</a> interface.

This callback interface enables applications to get synchronous notification about changes to the overlay position, size, visibility, and so on, so that the application can adjust its video visibility, size, and position. This avoids any color key flash at the beginning, end, or during playback. The application must implement the interface. It is important that none of the methods block or slow down the video processing, because this will cause problems with playback.

Use this interface if you are writing a filter that supports <b>IDDrawExclModeVideo</b> or needs to generate callbacks to enable an application to draw color keys at the right time.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDDrawExclModeVideoCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDDrawExclModeVideoCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDDrawExclModeVideoCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87d4a4b5-f67e-46f6-956a-1c9c309bfde7">OnUpdateColorKey</a>
</td>
<td align="left" width="63%">
Informs the application that the color key has changed so that the application can use the new color key to overlay graphics on the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ede823ba-8340-4339-8e8a-e1d4f9ad1273">OnUpdateOverlay</a>
</td>
<td align="left" width="63%">
Informs the application when the overlay surface for the video is about to change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00ddf110-8efc-414f-abfa-d6c7a22751a8">OnUpdateSize</a>
</td>
<td align="left" width="63%">
Informs the application when the size of the video rectangle is about to change.

</td>
</tr>
</table> 

