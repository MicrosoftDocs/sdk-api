---
UID: NF:mfreadwrite.IMFSinkWriter.SendStreamTick
title: IMFSinkWriter::SendStreamTick
author: windows-sdk-content
description: Indicates a gap in an input stream.
old-location: mf\imfsinkwriter_sendstreamtick.htm
old-project: medfound
ms.assetid: 3b4b76b7-1a39-4323-94e7-0b2d159a8038
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFSinkWriter interface [Media Foundation],SendStreamTick method, IMFSinkWriter.SendStreamTick, IMFSinkWriter::SendStreamTick, SendStreamTick, SendStreamTick method [Media Foundation], SendStreamTick method [Media Foundation],IMFSinkWriter interface, mf.imfsinkwriter_sendstreamtick, mfreadwrite/IMFSinkWriter::SendStreamTick
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSinkWriter.SendStreamTick
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSinkWriter::SendStreamTick


## -description


Indicates a gap in an input stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream.


### -param llTimestamp [in]

The position in the stream where the gap in the data occurs. The value is given in 100-nanosecond units, relative to the start of the stream.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For video, call this method once for each missing frame. For audio, call this method at least once per second during a gap in the audio. Set the <a href="https://msdn.microsoft.com/f9e1e700-9958-404d-8b83-08f846f5a1b0">MFSampleExtension_Discontinuity</a> attribute on the first media sample after the gap.

Internally, this method calls <a href="https://msdn.microsoft.com/bfa4fb12-59b2-4599-b8ff-dc38750a5a79">IMFStreamSink::PlaceMarker</a> on the media sink.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a>
 

 

