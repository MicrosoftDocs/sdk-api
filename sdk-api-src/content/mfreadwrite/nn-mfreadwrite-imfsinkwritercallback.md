---
UID: NN:mfreadwrite.IMFSinkWriterCallback
title: IMFSinkWriterCallback (mfreadwrite.h)

description: Callback interface for the Microsoft Media Foundation sink writer.
old-location: mf\imfsinkwritercallback.htm
tech.root: medfound
ms.assetid: fa0295e6-473d-4304-9a7b-24584cade0a0

ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback, IMFSinkWriterCallback interface [Media Foundation], IMFSinkWriterCallback interface [Media Foundation],described, mf.imfsinkwritercallback, mfreadwrite/IMFSinkWriterCallback
ms.topic: interface
f1_keywords: 
 - "mfreadwrite/IMFSinkWriterCallback"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSinkWriterCallback interface


## -description


Callback interface for the Microsoft Media Foundation sink writer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriterCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback-onfinalize">OnFinalize</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize">IMFSinkWriter::Finalize</a> method completes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwritercallback-onmarker">OnMarker</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-placemarker">IMFSinkWriter::PlaceMarker</a> method completes.

</td>
</tr>
</table> 


## -remarks



Set the callback pointer by setting the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-sink-writer-async-callback">MF_SINK_WRITER_ASYNC_CALLBACK</a> attribute when you first create the sink writer.



The callback methods can be called from any thread, so an object that implements this interface must be thread-safe.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sink-writer">Sink Writer</a>
 

 

