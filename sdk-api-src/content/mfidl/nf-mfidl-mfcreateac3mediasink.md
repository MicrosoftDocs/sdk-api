---
UID: NF:mfidl.MFCreateAC3MediaSink
title: MFCreateAC3MediaSink function
author: windows-sdk-content
description: Creates an instance of the AC-3 media sink.
old-location: mf\mfcreateac3mediasink.htm
old-project: medfound
ms.assetid: 49203EBF-24F3-4D9D-85EC-77BD8780BB41
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFCreateAC3MediaSink, MFCreateAC3MediaSink function [Media Foundation], mf.mfcreateac3mediasink, mfidl/MFCreateAC3MediaSink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateAC3MediaSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateAC3MediaSink function


## -description


Creates an instance of the AC-3 media sink.


## -parameters




### -param pTargetByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. The media sink writes the AC-3 file to this byte stream. The byte stream must be writable.




### -param pAudioMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. This parameter specifies the media type for the AC-3 audio stream. The media type must contain the following attributes.

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
<td><b>MFAudioFormat_Dolby_AC3</b> or <b>MFAudioFormat_Dolby_DDPlus</b></td>
</tr>
</table>
 


### -param ppMediaSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The AC-3 media sink takes compressed AC-3 audio as input and writes the audio to the  byte stream without modification. The primary use for this media sink is to stream AC-3 audio over a network. The media sink does not perform AC-3 audio encoding.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

