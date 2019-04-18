---
UID: NN:dwrite_3.IDWriteFontDownloadQueue
title: IDWriteFontDownloadQueue (dwrite_3.h)
author: windows-sdk-content
description: Interface that enqueues download requests for remote fonts, characters, glyphs, and font fragments.
old-location: directwrite\idwritefontdownloadqueue.htm
tech.root: DirectWrite
ms.assetid: d1b1dfab-a22a-40bb-ffc4-eb094ac14217
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontDownloadQueue, IDWriteFontDownloadQueue interface [Direct Write], IDWriteFontDownloadQueue interface [Direct Write],described, directwrite.idwritefontdownloadqueue, dwrite_3/IDWriteFontDownloadQueue
ms.topic: interface
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontDownloadQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontDownloadQueue interface


## -description


Interface that enqueues download requests for remote fonts, characters, glyphs, and font fragments.
        Provides methods to asynchronously execute a download, cancel pending downloads, and be notified of
        download completion. Callbacks to listeners will occur on the downloading thread, and objects must
        be must be able to handle calls on their methods from other threads at any time.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontDownloadQueue</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontDownloadQueue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontDownloadQueue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c539be2d-bc77-cc8a-c78c-226a67b8dd26">AddListener</a>
</td>
<td align="left" width="63%">
Registers a client-defined listener object that receives download notifications.  
    All registered listener's DownloadCompleted will be called after <a href="https://msdn.microsoft.com/1e3b200c-0190-f600-1cb6-4e2a46f882b4">BeginDownload</a>completes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e3b200c-0190-f600-1cb6-4e2a46f882b4">BeginDownload</a>
</td>
<td align="left" width="63%">
Begins an asynchronous download operation. The download operation executes   
    in the background until it completes or is cancelled by a <a href="https://msdn.microsoft.com/f2ecabcf-3301-d446-8eda-4536b3f9b5e3">CancelDownload</a> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2ecabcf-3301-d446-8eda-4536b3f9b5e3">CancelDownload</a>
</td>
<td align="left" width="63%">
 Removes all download requests from the queue and cancels any active download    
    operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fbbe575-b186-7ffb-ff32-efceccccc48c">GetGenerationCount</a>
</td>
<td align="left" width="63%">
Gets the current generation number of the download queue, which is incremented   
    every time after a download completes, whether failed or successful. This cookie  
    value can be compared against cached data to determine if it is stale.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f1f0d1c-0db8-c382-7879-92a889cfeb6b">IsEmpty</a>
</td>
<td align="left" width="63%">
Determines whether the download queue is empty. Note that the queue does not    
    include requests that are already being downloaded. Calling <a href="https://msdn.microsoft.com/1e3b200c-0190-f600-1cb6-4e2a46f882b4">BeginDownload</a>clears the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3470f17-9630-de53-d1ae-ab2a2508a069">RemoveListener</a>
</td>
<td align="left" width="63%">
Unregisters a notification handler that was previously registered using <a href="https://msdn.microsoft.com/c539be2d-bc77-cc8a-c78c-226a67b8dd26">AddListener</a>.

</td>
</tr>
</table> 

