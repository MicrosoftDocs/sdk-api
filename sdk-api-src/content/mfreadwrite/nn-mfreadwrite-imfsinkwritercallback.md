---
UID: NN:mfreadwrite.IMFSinkWriterCallback
title: IMFSinkWriterCallback (mfreadwrite.h)
author: windows-sdk-content
description: Callback interface for the Microsoft Media Foundation sink writer.
old-location: mf\imfsinkwritercallback.htm
tech.root: medfound
ms.assetid: fa0295e6-473d-4304-9a7b-24584cade0a0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFSinkWriterCallback, IMFSinkWriterCallback interface [Media Foundation], IMFSinkWriterCallback interface [Media Foundation],described, mf.imfsinkwritercallback, mfreadwrite/IMFSinkWriterCallback
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
 - IMFSinkWriterCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriterCallback interface


## -description


Callback interface for the Microsoft Media Foundation sink writer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSinkWriterCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriterCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9da7bb55-bf9f-4579-ae8e-b33ce5461950">OnFinalize</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://msdn.microsoft.com/352e6679-0710-429a-a659-47044ab60773">IMFSinkWriter::Finalize</a> method completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b1ca6a7-c2bc-4b30-aa86-05bd4ccc052c">OnMarker</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://msdn.microsoft.com/93140993-a926-437e-bc40-9b011c4c6832">IMFSinkWriter::PlaceMarker</a> method completes.

</td>
</tr>
</table> 


## -remarks



Set the callback pointer by setting the <a href="https://msdn.microsoft.com/22df1fa0-469d-4501-aaf0-a0379b7ed096">MF_SINK_WRITER_ASYNC_CALLBACK</a> attribute when you first create the sink writer.



The callback methods can be called from any thread, so an object that implements this interface must be thread-safe.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

