---
UID: NF:mfidl.MFCreateTranscodeTopologyFromByteStream
title: MFCreateTranscodeTopologyFromByteStream function (mfidl.h)
author: windows-sdk-content
description: Creates a topology for transcoding to a byte stream.
old-location: mf\mfcreatetranscodetopologyfrombytestream.htm
tech.root: medfound
ms.assetid: FBA9E0A1-7763-4566-8245-D626C82D0355
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCreateTranscodeTopologyFromByteStream, MFCreateTranscodeTopologyFromByteStream function [Media Foundation], mf.mfcreatetranscodetopologyfrombytestream, mfidl/MFCreateTranscodeTopologyFromByteStream
ms.topic: function
f1_keywords: 
 - "mfidl/MFCreateTranscodeTopologyFromByteStream"
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
 - MFCreateTranscodeTopologyFromByteStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateTranscodeTopologyFromByteStream function


## -description


Creates a topology for transcoding to a byte stream.


## -parameters




### -param pSrc [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface of a media source. The media source provides that source content for transcoding.


### -param pOutputStream [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The transcoded output will be written to this byte stream.


### -param pProfile [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile">IMFTranscodeProfile</a> interface of a transcoding profile. 


### -param ppTranscodeTopo [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a partial topology that contains the media source, the encoder, and the media sink. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>
 

 

