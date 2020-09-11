---
UID: NN:mfreadwrite.IMFSourceReader
title: IMFSourceReader (mfreadwrite.h)
description: Implemented by the Microsoft Media Foundation source reader object.
helpviewer_keywords: ["IMFSourceReader","IMFSourceReader interface [Media Foundation]","IMFSourceReader interface [Media Foundation]","described","mf.imfsourcereader","mfreadwrite/IMFSourceReader"]
old-location: mf\imfsourcereader.htm
tech.root: mf
ms.assetid: 7d3cc314-6b9e-437c-afda-ee1965a12721
ms.date: 12/05/2018
ms.keywords: IMFSourceReader, IMFSourceReader interface [Media Foundation], IMFSourceReader interface [Media Foundation],described, mf.imfsourcereader, mfreadwrite/IMFSourceReader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceReader
 - mfreadwrite/IMFSourceReader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReader
---

# IMFSourceReader interface


## -description

Implemented by the Microsoft Media Foundation source reader object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceReader</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush">Flush</a>
</td>
<td align="left" width="63%">
Flushes one or more streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype">GetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Gets the current media type for a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype">GetNativeMediaType</a>
</td>
<td align="left" width="63%">
Gets a format that is supported natively by the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute">GetPresentationAttribute</a>
</td>
<td align="left" width="63%">
Gets an attribute from the underlying media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream">GetServiceForStream</a>
</td>
<td align="left" width="63%">
Queries the underlying media source or decoder for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getstreamselection">GetStreamSelection</a>
</td>
<td align="left" width="63%">
Queries whether a stream is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample">ReadSample</a>
</td>
<td align="left" width="63%">
Reads the next sample from the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype">SetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition">SetCurrentPosition</a>
</td>
<td align="left" width="63%">
Seeks to a new position in the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection">SetStreamSelection</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream">MFCreateSourceReaderFromByteStream</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource">MFCreateSourceReaderFromMediaSource</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl">MFCreateSourceReaderFromURL</a>
</li>
</ul>
Alternatively, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory">IMFReadWriteClassFactory</a> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

In Windows 8, this interface is extended with <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex">IMFSourceReaderEx</a>.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a>

