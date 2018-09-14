---
UID: NF:mfcaptureengine.IMFCaptureSource.GetMirrorState
title: IMFCaptureSource::GetMirrorState
author: windows-sdk-content
description: Gets the current mirroring state of the video preview stream.
old-location: mf\imfcapturesource_getmirrorstate.htm
tech.root: medfound
ms.assetid: 3FB15EC5-DE9C-4051-9FBA-7CE332E70078
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetMirrorState, GetMirrorState method [Media Foundation], GetMirrorState method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetMirrorState method, IMFCaptureSource.GetMirrorState, IMFCaptureSource::GetMirrorState, mf.imfcapturesource_getmirrorstate, mf.imfcapturesource_getpreviewmirrorstate, mfcaptureengine/IMFCaptureSource::GetMirrorState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfcaptureengine.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSource.GetMirrorState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetMirrorState


## -description


Gets the current mirroring state of the video preview stream.


## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream.


### -param pfMirrorState [out]

Receives the value <b>TRUE</b> if mirroring is enabled, or <b>FALSE</b> if mirroring is disabled.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

