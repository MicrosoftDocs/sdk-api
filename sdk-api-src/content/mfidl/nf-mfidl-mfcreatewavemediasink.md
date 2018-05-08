---
UID: NF:mfidl.MFCreateWAVEMediaSink
title: MFCreateWAVEMediaSink function
author: windows-driver-content
description: Creates an WAVE archive sink. The WAVE archive sink takes audio and writes it to an .wav file.
old-location: mf\mfcreatewavemediasink.htm
old-project: medfound
ms.assetid: AF2FAE46-E7A0-4294-8EE1-499AE11CD1E3
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: MFCreateWAVEMediaSink, MFCreateWAVEMediaSink function [Media Foundation], mf.mfcreatewavemediasink, mfidl/MFCreateWAVEMediaSink
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateWAVEMediaSink
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateWAVEMediaSink function


## -description


 Creates an WAVE archive sink.  The WAVE archive sink takes
audio and writes it to an .wav file.



## -parameters




### -param pTargetByteStream [in]

 Pointer to the byte stream that will be used to write the .wav file.


### -param pAudioMediaType [in]

Pointer to the audio media type.


### -param ppMediaSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface.  The caller must release this interface.


## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

