---
UID: NF:mfidl.MFCreateAC3MediaSink
title: MFCreateAC3MediaSink function (mfidl.h)
description: Creates an instance of the AC-3 media sink.
helpviewer_keywords: ["MFCreateAC3MediaSink","MFCreateAC3MediaSink function [Media Foundation]","mf.mfcreateac3mediasink","mfidl/MFCreateAC3MediaSink"]
old-location: mf\mfcreateac3mediasink.htm
tech.root: medfound
ms.assetid: 49203EBF-24F3-4D9D-85EC-77BD8780BB41
ms.date: 12/05/2018
ms.keywords: MFCreateAC3MediaSink, MFCreateAC3MediaSink function [Media Foundation], mf.mfcreateac3mediasink, mfidl/MFCreateAC3MediaSink
f1_keywords:
- mfidl/MFCreateAC3MediaSink
dev_langs:
- c++
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
req.lib: 
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
- MFCreateAC3MediaSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateAC3MediaSink function


## -description


Creates an instance of the AC-3 media sink.


## -parameters




### -param pTargetByteStream [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The media sink writes the AC-3 file to this byte stream. The byte stream must be writable.




### -param pAudioMediaType [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. This parameter specifies the media type for the AC-3 audio stream. The media type must contain the following attributes.

<table>
<tr>
<th>Attribute</th>
<th>Value</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-major-type-attribute">MF_MT_MAJOR_TYPE</a>
</td>
<td><b>MFMediaType_Audio</b></td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-subtype-attribute">MF_MT_SUBTYPE</a>
</td>
<td><b>MFAudioFormat_Dolby_AC3</b> or <b>MFAudioFormat_Dolby_DDPlus</b></td>
</tr>
</table>
 


### -param ppMediaSink [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The AC-3 media sink takes compressed AC-3 audio as input and writes the audio to the  byte stream without modification. The primary use for this media sink is to stream AC-3 audio over a network. The media sink does not perform AC-3 audio encoding.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

