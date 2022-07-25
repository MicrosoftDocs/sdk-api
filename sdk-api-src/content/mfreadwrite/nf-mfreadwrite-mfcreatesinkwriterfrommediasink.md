---
UID: NF:mfreadwrite.MFCreateSinkWriterFromMediaSink
title: MFCreateSinkWriterFromMediaSink function (mfreadwrite.h)
description: Creates the sink writer from a media sink.
helpviewer_keywords: ["MFCreateSinkWriterFromMediaSink","MFCreateSinkWriterFromMediaSink function [Media Foundation]","mf.mfcreatesinkwriterfrommediasink","mfreadwrite/MFCreateSinkWriterFromMediaSink"]
old-location: mf\mfcreatesinkwriterfrommediasink.htm
tech.root: mf
ms.assetid: 77bd81fe-bcbd-4bcd-9d3a-dd9fe6154337
ms.date: 12/05/2018
ms.keywords: MFCreateSinkWriterFromMediaSink, MFCreateSinkWriterFromMediaSink function [Media Foundation], mf.mfcreatesinkwriterfrommediasink, mfreadwrite/MFCreateSinkWriterFromMediaSink
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
 - MFCreateSinkWriterFromMediaSink
 - mfreadwrite/MFCreateSinkWriterFromMediaSink
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
 - MFCreateSinkWriterFromMediaSink
---

# MFCreateSinkWriterFromMediaSink function


## -description

Creates the sink writer from a media sink.

## -parameters

### -param pMediaSink [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface of a media sink.

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. You can use this parameter to configure the sink writer. For more information, see <a href="/windows/desktop/medfound/sink-writer-attributes">Sink Writer Attributes</a>. This parameter can be <b>NULL</b>.

### -param ppSinkWriter [out]

Receives a pointer to the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call <b>CoInitialize(Ex)</b> and <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> before calling this function.

When you are done using the media sink, call the media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">IMFMediaSink::Shutdown</a> method. (The sink writer does not shut down the media sink.) Release the sink writer before calling <b>Shutdown</b> on the media sink.

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>