---
UID: NF:mfidl.MFCreateFMPEG4MediaSink
title: MFCreateFMPEG4MediaSink function
author: windows-sdk-content
description: Creates a media sink for authoring fragmented MP4 files.
old-location: mf\mfcreatefmpeg4mediasink.htm
tech.root: medfound
ms.assetid: 31FDA8BD-C837-4CA4-8635-D4A7B53AC7AC
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFCreateFMPEG4MediaSink, MFCreateFMPEG4MediaSink function [Media Foundation], mf.mfcreatefmpeg4mediasink, mfidl/MFCreateFMPEG4MediaSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateFMPEG4MediaSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateFMPEG4MediaSink function


## -description


Creates a media sink for authoring fragmented MP4 files.


## -parameters




### -param pIByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream.  The media sink writes the MP4 file to this byte stream. The byte stream must be writable and support seeking.


### -param pVideoMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of a video media type. This type specifies the format of the video stream.

This parameter can be <b>NULL</b>, but not if <i>pAudioMediaType</i> is <b>NULL</b>.


### -param pAudioMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of an audio media type. This type specifies the format of the audio stream.

This parameter can be <b>NULL</b>, but not if <i>pVideoMediaType</i> is <b>NULL</b>.


### -param ppIMediaSink [out]

Receives a pointer to the MP4 media sink's <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

