---
UID: NF:wmcodecdsp.IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame
title: IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame (wmcodecdsp.h)
description: Note  This method is obsolete and should not be used. Retrieves the current reconstructed video frame.
helpviewer_keywords: ["GetReconstructedVideoFrame","GetReconstructedVideoFrame method [Media Foundation]","GetReconstructedVideoFrame method [Media Foundation]","IWMVideoDecoderReconBuffer interface","IWMVideoDecoderReconBuffer interface [Media Foundation]","GetReconstructedVideoFrame method","IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame","IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame","codecapi.iwmvideodecoderreconbuffergetreconstructedvideoframe","mf.iwmvideodecoderreconbuffergetreconstructedvideoframe","wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame"]
old-location: mf\iwmvideodecoderreconbuffergetreconstructedvideoframe.htm
tech.root: mf
ms.assetid: 6e952923-2043-4b0d-b936-c570373a3544
ms.date: 12/05/2018
ms.keywords: GetReconstructedVideoFrame, GetReconstructedVideoFrame method [Media Foundation], GetReconstructedVideoFrame method [Media Foundation],IWMVideoDecoderReconBuffer interface, IWMVideoDecoderReconBuffer interface [Media Foundation],GetReconstructedVideoFrame method, IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame, IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame, codecapi.iwmvideodecoderreconbuffergetreconstructedvideoframe, mf.iwmvideodecoderreconbuffergetreconstructedvideoframe, wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame
 - wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame
---

# IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame


## -description

<div class="alert"><b>Note</b>  This method is obsolete and should not be used.</div>
<div> </div>
Retrieves the current reconstructed video frame.

## -parameters

### -param pBuf [out]

Address of a media buffer that receives the reconstructed video frame.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderreconbuffer">IWMVideoDecoderReconBuffer Interface</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderreconbuffer-getreconstructedvideoframesize">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderreconbuffer-setreconstructedvideoframe">IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame</a>