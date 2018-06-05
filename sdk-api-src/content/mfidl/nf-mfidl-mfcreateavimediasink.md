---
UID: NF:mfidl.MFCreateAVIMediaSink
title: MFCreateAVIMediaSink function
author: windows-sdk-content
description: Creates an Audio-Video Interleaved (AVI) Sink.
old-location: mf\mfcreateavimediasink.htm
old-project: medfound
ms.assetid: BAF47469-783B-4035-BD83-2921A88877E4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFCreateAVIMediaSink, MFCreateAVIMediaSink function [Media Foundation], mf.mfcreateavimediasink, mfidl/MFCreateAVIMediaSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateAVIMediaSink
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateAVIMediaSink function


## -description


Creates an Audio-Video Interleaved (AVI) Sink.


## -parameters




### -param pIByteStream [in]

Pointer to the byte stream that will be used to write the AVI file.


### -param pVideoMediaType [in]

Pointer to the media type of the video input stream


### -param pAudioMediaType [in, optional]

Pointer to the media type of the audio input stream


### -param ppIMediaSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> Interface.  The caller must release this interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

