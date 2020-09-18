---
UID: NF:wmcodecdsp.IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize
title: IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize (wmcodecdsp.h)
description: Note  This method is obsolete and should not be used. Retrieves the size of the current reconstructed video frame.
helpviewer_keywords: ["GetReconstructedVideoFrameSize","GetReconstructedVideoFrameSize method [Media Foundation]","GetReconstructedVideoFrameSize method [Media Foundation]","IWMVideoDecoderReconBuffer interface","IWMVideoDecoderReconBuffer interface [Media Foundation]","GetReconstructedVideoFrameSize method","IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize","IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize","codecapi.iwmvideodecoderreconbuffergetreconstructedvideoframesize","mf.iwmvideodecoderreconbuffergetreconstructedvideoframesize","wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize"]
old-location: mf\iwmvideodecoderreconbuffergetreconstructedvideoframesize.htm
tech.root: mf
ms.assetid: 7faadeed-4c89-4b3e-8e08-51de66224aaa
ms.date: 12/05/2018
ms.keywords: GetReconstructedVideoFrameSize, GetReconstructedVideoFrameSize method [Media Foundation], GetReconstructedVideoFrameSize method [Media Foundation],IWMVideoDecoderReconBuffer interface, IWMVideoDecoderReconBuffer interface [Media Foundation],GetReconstructedVideoFrameSize method, IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize, IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize, codecapi.iwmvideodecoderreconbuffergetreconstructedvideoframesize, mf.iwmvideodecoderreconbuffergetreconstructedvideoframesize, wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize
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
 - IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize
 - wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize
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
 - IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize
---

# IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize


## -description

<div class="alert"><b>Note</b>  This method is obsolete and should not be used.</div>
<div> </div>
Retrieves the size of the current reconstructed video frame.

## -parameters

### -param pdwSize [out]

Address of a variable that receives the frame size in bytes.

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



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderreconbuffer-getreconstructedvideoframe">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame</a>



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderreconbuffer-setreconstructedvideoframe">IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame</a>