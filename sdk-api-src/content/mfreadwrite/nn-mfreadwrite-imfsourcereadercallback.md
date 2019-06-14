---
UID: NN:mfreadwrite.IMFSourceReaderCallback
title: IMFSourceReaderCallback (mfreadwrite.h)
author: windows-sdk-content
description: Callback interface for the Microsoft Media Foundation source reader.
old-location: mf\imfsourcereadercallback.htm
tech.root: medfound
ms.assetid: fff8b6e6-5d56-4301-b3ce-f3ff49398593
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback, IMFSourceReaderCallback interface [Media Foundation], IMFSourceReaderCallback interface [Media Foundation],described, mf.imfsourcereadercallback, mfreadwrite/IMFSourceReaderCallback
ms.topic: interface
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfreadwrite.h
api_name:
 - IMFSourceReaderCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceReaderCallback interface


## -description


Callback interface for the Microsoft Media Foundation source reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReaderCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceReaderCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceReaderCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent">OnEvent</a>
</td>
<td align="left" width="63%">
Called when the source reader receives certain events from the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush">OnFlush</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush">IMFSourceReader::Flush</a> method completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample">OnReadSample</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">IMFSourceReader::ReadSample</a> method completes.

</td>
</tr>
</table> 


## -remarks



Use the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-source-reader-async-callback">MF_SOURCE_READER_ASYNC_CALLBACK</a> attribute to set the callback pointer when you first create the source reader object.

The callback methods can be called from any thread, so an object that implements this interface must be thread-safe.

If you do not specify a callback pointer, the source reader operates synchronously.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-source-reader-in-asynchronous-mode">Using the Source Reader in Asynchronous Mode</a>
 

 

