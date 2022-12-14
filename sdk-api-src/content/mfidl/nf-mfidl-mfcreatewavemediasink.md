---
UID: NF:mfidl.MFCreateWAVEMediaSink
title: MFCreateWAVEMediaSink function (mfidl.h)
description: Creates an WAVE archive sink. The WAVE archive sink takes audio and writes it to an .wav file.
helpviewer_keywords: ["MFCreateWAVEMediaSink","MFCreateWAVEMediaSink function [Media Foundation]","mf.mfcreatewavemediasink","mfidl/MFCreateWAVEMediaSink"]
old-location: mf\mfcreatewavemediasink.htm
tech.root: mf
ms.assetid: AF2FAE46-E7A0-4294-8EE1-499AE11CD1E3
ms.date: 12/05/2018
ms.keywords: MFCreateWAVEMediaSink, MFCreateWAVEMediaSink function [Media Foundation], mf.mfcreatewavemediasink, mfidl/MFCreateWAVEMediaSink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateWAVEMediaSink
 - mfidl/MFCreateWAVEMediaSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateWAVEMediaSink
---

# MFCreateWAVEMediaSink function


## -description

 Creates a WAVE archive sink.  The WAVE archive sink takes
audio and writes it to an .wav file.

## -parameters

### -param pTargetByteStream [in]

 Pointer to the byte stream that will be used to write the .wav file.

### -param pAudioMediaType [in]

Pointer to the audio media type.

### -param ppMediaSink [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface.  The caller must release this interface.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>