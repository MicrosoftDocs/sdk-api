---
UID: NN:mfreadwrite.IMFReadWriteClassFactory
title: IMFReadWriteClassFactory (mfreadwrite.h)
description: Creates an instance of either the sink writer or the source reader.
helpviewer_keywords: ["IMFReadWriteClassFactory","IMFReadWriteClassFactory interface [Media Foundation]","IMFReadWriteClassFactory interface [Media Foundation]","described","mf.imfreadwriteclassfactory","mfreadwrite/IMFReadWriteClassFactory"]
old-location: mf\imfreadwriteclassfactory.htm
tech.root: mf
ms.assetid: 83ef0f0a-ae60-474d-a9e7-7c83a73f6255
ms.date: 12/05/2018
ms.keywords: IMFReadWriteClassFactory, IMFReadWriteClassFactory interface [Media Foundation], IMFReadWriteClassFactory interface [Media Foundation],described, mf.imfreadwriteclassfactory, mfreadwrite/IMFReadWriteClassFactory
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
 - IMFReadWriteClassFactory
 - mfreadwrite/IMFReadWriteClassFactory
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
 - IMFReadWriteClassFactory
---

# IMFReadWriteClassFactory interface


## -description

Creates an instance of either the sink writer or the source reader.

## -inheritance

The <b>IMFReadWriteClassFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFReadWriteClassFactory</b> also has these types of members:

## -remarks

To get a pointer to this interface, call the <b>CoCreateInstance</b> function. The CLSID is <b>CLSID_MFReadWriteClassFactory</b>. Call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> function before using  the interface.

As an alternative to using this interface, you can call any of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink">MFCreateSinkWriterFromMediaSink</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl">MFCreateSinkWriterFromURL</a>
</li>
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
Internally, these functions use the <b>IMFReadWriteClassFactory</b> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
