---
UID: NN:mfreadwrite.IMFSinkWriter
title: IMFSinkWriter (mfreadwrite.h)
description: Implemented by the Microsoft Media Foundation sink writer object.
helpviewer_keywords: ["IMFSinkWriter","IMFSinkWriter interface [Media Foundation]","IMFSinkWriter interface [Media Foundation]","described","mf.imfsinkwriter","mfreadwrite/IMFSinkWriter"]
old-location: mf\imfsinkwriter.htm
tech.root: mf
ms.assetid: 76fb915e-1586-429a-88a5-bd1290799352
ms.date: 12/05/2018
ms.keywords: IMFSinkWriter, IMFSinkWriter interface [Media Foundation], IMFSinkWriter interface [Media Foundation],described, mf.imfsinkwriter, mfreadwrite/IMFSinkWriter
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
 - IMFSinkWriter
 - mfreadwrite/IMFSinkWriter
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
 - IMFSinkWriter
---

# IMFSinkWriter interface


## -description

Implemented by the Microsoft Media Foundation sink writer object.

## -inheritance

The <b>IMFSinkWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriter</b> also has these types of members:

## -remarks

To create the sink writer, call one of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink">MFCreateSinkWriterFromMediaSink</a>
</li>
<li>
<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl">MFCreateSinkWriterFromURL</a>
</li>
</ul>
Alternatively, use the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory">IMFReadWriteClassFactory</a> interface.

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

In Windows 8, this interface is extended with <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>
