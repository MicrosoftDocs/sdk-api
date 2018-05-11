---
UID: NN:mfreadwrite.IMFReadWriteClassFactory
title: IMFReadWriteClassFactory
author: windows-driver-content
description: Creates an instance of either the sink writer or the source reader.
old-location: mf\imfreadwriteclassfactory.htm
old-project: medfound
ms.assetid: 83ef0f0a-ae60-474d-a9e7-7c83a73f6255
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFReadWriteClassFactory, IMFReadWriteClassFactory interface [Media Foundation], IMFReadWriteClassFactory interface [Media Foundation],described, mf.imfreadwriteclassfactory, mfreadwrite/IMFReadWriteClassFactory
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFReadWriteClassFactory
product: Windows
targetos: Windows
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFReadWriteClassFactory interface


## -description


Creates an instance of either the sink writer or the source reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFReadWriteClassFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFReadWriteClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFReadWriteClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5da582c2-37f9-47ee-b8ea-d21f1323f1df">CreateInstanceFromObject</a>
</td>
<td align="left" width="63%">
Creates an instance of the sink writer or source reader, given an <b>IUnknown</b> pointer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2769faa2-e381-4908-95f8-122ae4cd7ec5">CreateInstanceFromURL</a>
</td>
<td align="left" width="63%">
Creates an instance of the sink writer or source reader, given a URL.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call the <b>CoCreateInstance</b> function. The CLSID is <b>CLSID_MFReadWriteClassFactory</b>. Call the <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> function before using  the interface.

As an alternative to using this interface, you can call any of the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/77bd81fe-bcbd-4bcd-9d3a-dd9fe6154337">MFCreateSinkWriterFromMediaSink</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ac6a30c7-5e44-453a-8114-8d7d65332024">MFCreateSinkWriterFromURL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e167159d-902c-4c34-b5f0-eb764fe2de1c">MFCreateSourceReaderFromByteStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/924e1813-b025-435b-9770-52503a9eb619">MFCreateSourceReaderFromMediaSource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/060b4ab3-9a9f-4c90-a8c5-9c6d81877e2f">MFCreateSourceReaderFromURL</a>
</li>
</ul>
Internally, these functions use the <b>IMFReadWriteClassFactory</b> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

