---
UID: NF:mfreadwrite.MFCreateSourceReaderFromByteStream
title: MFCreateSourceReaderFromByteStream function (mfreadwrite.h)
description: Creates the source reader from a byte stream.
helpviewer_keywords: ["MFCreateSourceReaderFromByteStream","MFCreateSourceReaderFromByteStream function [Media Foundation]","mf.mfcreatesourcereaderfrombytestream","mfreadwrite/MFCreateSourceReaderFromByteStream"]
old-location: mf\mfcreatesourcereaderfrombytestream.htm
tech.root: mf
ms.assetid: e167159d-902c-4c34-b5f0-eb764fe2de1c
ms.date: 12/05/2018
ms.keywords: MFCreateSourceReaderFromByteStream, MFCreateSourceReaderFromByteStream function [Media Foundation], mf.mfcreatesourcereaderfrombytestream, mfreadwrite/MFCreateSourceReaderFromByteStream
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
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateSourceReaderFromByteStream
 - mfreadwrite/MFCreateSourceReaderFromByteStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfreadwrite.dll
api_name:
 - MFCreateSourceReaderFromByteStream
---

# MFCreateSourceReaderFromByteStream function


## -description

Creates the source reader from a byte stream.

## -parameters

### -param pByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. This byte stream will provide the source data for the source reader.

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this parameter to configure the source reader. For more information, see <a href="/windows/desktop/medfound/source-reader-attributes">Source Reader Attributes</a>. This parameter can be <b>NULL</b>.

### -param ppSourceReader [out]

Receives a pointer to the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call <b>CoInitialize(Ex)</b> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> before calling this function.

Internally, the source reader calls the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream">IMFSourceResolver::CreateObjectFromByteStream</a> method to create a media source from the byte stream. Therefore, a byte-stream handler must be registered for the byte stream. For more information about byte-stream handlers, see <a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>.
      

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/source-reader">Source Reader</a>