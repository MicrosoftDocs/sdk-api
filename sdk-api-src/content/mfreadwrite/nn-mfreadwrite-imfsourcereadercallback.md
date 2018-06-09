---
UID: NN:mfreadwrite.IMFSourceReaderCallback
title: IMFSourceReaderCallback
author: windows-sdk-content
description: Callback interface for the Microsoft Media Foundation source reader.
old-location: mf\imfsourcereadercallback.htm
old-project: medfound
ms.assetid: fff8b6e6-5d56-4301-b3ce-f3ff49398593
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFSourceReaderCallback, IMFSourceReaderCallback interface [Media Foundation], IMFSourceReaderCallback interface [Media Foundation],described, mf.imfsourcereadercallback, mfreadwrite/IMFSourceReaderCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MF_SOURCE_READER_FLAG
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
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceReaderCallback interface


## -description


Callback interface for the Microsoft Media Foundation source reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReaderCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceReaderCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cbe85d0f-26a1-4526-bfe6-b6183812a271">OnEvent</a>
</td>
<td align="left" width="63%">
Called when the source reader receives certain events from the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8273b0a-a75a-453f-bb42-38d554e44262">OnFlush</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://msdn.microsoft.com/34992c64-9956-4b23-a979-df7f678405b5">IMFSourceReader::Flush</a> method completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f334b49-d297-478d-a037-2fc53a75ed52">OnReadSample</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> method completes.

</td>
</tr>
</table> 


## -remarks



Use the <a href="https://msdn.microsoft.com/de226a5a-03c0-4bfe-bb20-8969ce43cf53">MF_SOURCE_READER_ASYNC_CALLBACK</a> attribute to set the callback pointer when you first create the source reader object.

The callback methods can be called from any thread, so an object that implements this interface must be thread-safe.

If you do not specify a callback pointer, the source reader operates synchronously.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>



<a href="https://msdn.microsoft.com/9D3C2780-D7DB-4151-8474-9A19EC94F6BE">Using the Source Reader in Asynchronous Mode</a>
 

 

