---
UID: NF:mfidl.MFCreateADTSMediaSink
title: MFCreateADTSMediaSink function
author: windows-driver-content
description: Creates an instance of the audio data transport stream (ADTS) media sink.
old-location: mf\mfcreateadtsmediasink.htm
old-project: medfound
ms.assetid: 18B2F5C7-61A6-447B-9BC8-2394A68BA777
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: MFCreateADTSMediaSink, MFCreateADTSMediaSink function [Media Foundation], mf.mfcreateadtsmediasink, mfidl/MFCreateADTSMediaSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateADTSMediaSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateADTSMediaSink function


## -description


Creates an instance of the audio data transport stream (ADTS) media sink.


## -parameters




### -param pTargetByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. The media sink writes the ADTS stream to this byte stream. The byte stream must be writable.


### -param pAudioMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. This parameter specifies the media type for the ADTS stream. The media type must contain the following attributes.

<table>
<tr>
<th>Attribute</th>
<th>Value</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b88b5fcf-8025-4638-930d-9fc5cf0ec8a3">MF_MT_MAJOR_TYPE</a>
</td>
<td><b>MFMediaType_Audio</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8e600943-92f1-4936-8c00-842fc7f4cb57">MF_MT_SUBTYPE</a>
</td>
<td><b>MFAudioFormat_AAC</b></td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a032fcf4-2584-4047-adbd-d94d4fc4e841">MF_MT_AAC_PAYLOAD_TYPE</a>
</td>
<td>0 (raw AAC) or 1 (ADTS)</td>
</tr>
</table>
 


### -param ppMediaSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ADTS media sink converts Advanced Audio Coding (AAC) audio packets into an ADTS stream. The primary use for this media sink is to stream ADTS over a network. The output is not an audio file, but a stream of audio frames with ADTS headers.

The media sink can accept raw AAC frames (<a href="https://msdn.microsoft.com/a032fcf4-2584-4047-adbd-d94d4fc4e841">MF_MT_AAC_PAYLOAD_TYPE</a> = 0) or ADTS packets (MF_MT_AAC_PAYLOAD_TYPE = 1). If the input is raw AAC, the media sink inserts an ADTS header at the start of each audio frame. If the input is ADTS packets, the media sink passes the packets through to the byte stream, without modification.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

