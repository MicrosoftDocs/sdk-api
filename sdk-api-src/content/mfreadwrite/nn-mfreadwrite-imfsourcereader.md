---
UID: NN:mfreadwrite.IMFSourceReader
title: IMFSourceReader
author: windows-driver-content
description: Implemented by the Microsoft Media Foundation source reader object.
old-location: mf\imfsourcereader.htm
old-project: medfound
ms.assetid: 7d3cc314-6b9e-437c-afda-ee1965a12721
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMFSourceReader, IMFSourceReader interface [Media Foundation], IMFSourceReader interface [Media Foundation],described, mf.imfsourcereader, mfreadwrite/IMFSourceReader
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
-	IMFSourceReader
product: Windows
targetos: Windows
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceReader interface


## -description


Implemented by the Microsoft Media Foundation source reader object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Flushes one or more streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0fe3b34-42ad-45e4-812d-679bbe01a200">GetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Gets the current media type for a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b514f8d-082f-4e84-b512-d4a59706a6d8">GetNativeMediaType</a>
</td>
<td align="left" width="63%">
Gets a format that is supported natively by the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40544e1e-cce2-4860-aeb2-b60696b09145">GetPresentationAttribute</a>
</td>
<td align="left" width="63%">
Gets an attribute from the underlying media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8868e4d-eedd-4fbd-b870-d3af48890c92">GetServiceForStream</a>
</td>
<td align="left" width="63%">
Queries the underlying media source or decoder for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40301426-4bf2-442c-91b5-9916d1314617">GetStreamSelection</a>
</td>
<td align="left" width="63%">
Queries whether a stream is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">ReadSample</a>
</td>
<td align="left" width="63%">
Reads the next sample from the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54caec4d-1393-487b-94ee-78563b2b4645">SetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9412f5-4f2f-463d-9988-80e706afd9c4">SetCurrentPosition</a>
</td>
<td align="left" width="63%">
Seeks to a new position in the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5efadce6-347c-48cf-b42c-d461922b2523">SetStreamSelection</a>
</td>
<td align="left" width="63%">
Selects or deselects one or more streams.

</td>
</tr>
</table> 


## -remarks



To create the source reader, call one of the following functions:

<ul>
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
Alternatively, use the <a href="https://msdn.microsoft.com/83ef0f0a-ae60-474d-a9e7-7c83a73f6255">IMFReadWriteClassFactory</a> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

In Windows 8, this interface is extended with <a href="https://msdn.microsoft.com/59888F9B-C464-4045-AA77-03EE16E2B598">IMFSourceReaderEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

