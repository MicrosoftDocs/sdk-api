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

The <b>IMFSourceReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceReader</b> also has these types of members:

## -remarks

To create the source reader, call one of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream">MFCreateSourceReaderFromByteStream</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource">MFCreateSourceReaderFromMediaSource</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl">MFCreateSourceReaderFromURL</a>
</li>
</ul>
Alternatively, use the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory">IMFReadWriteClassFactory</a> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

In Windows 8, this interface is extended with <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex">IMFSourceReaderEx</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>
