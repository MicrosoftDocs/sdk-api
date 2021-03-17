---
UID: NF:wmcodecdsp.IWMVideoDecoderReconBuffer.SetReconstructedVideoFrame
title: IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame (wmcodecdsp.h)
description: Note  This method is obsolete and should not be used. Restores the current reconstructed video frame.
helpviewer_keywords: ["IWMVideoDecoderReconBuffer interface [Media Foundation]","SetReconstructedVideoFrame method","IWMVideoDecoderReconBuffer.SetReconstructedVideoFrame","IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame","SetReconstructedVideoFrame","SetReconstructedVideoFrame method [Media Foundation]","SetReconstructedVideoFrame method [Media Foundation]","IWMVideoDecoderReconBuffer interface","codecapi.iwmvideodecoderreconbuffersetreconstructedvideoframe","mf.iwmvideodecoderreconbuffersetreconstructedvideoframe","wmcodecdsp/IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame"]
old-location: mf\iwmvideodecoderreconbuffersetreconstructedvideoframe.htm
tech.root: mf
ms.assetid: baffb56f-b2c5-464f-a2ae-1cb9677b8b83
ms.date: 12/05/2018
ms.keywords: IWMVideoDecoderReconBuffer interface [Media Foundation],SetReconstructedVideoFrame method, IWMVideoDecoderReconBuffer.SetReconstructedVideoFrame, IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame, SetReconstructedVideoFrame, SetReconstructedVideoFrame method [Media Foundation], SetReconstructedVideoFrame method [Media Foundation],IWMVideoDecoderReconBuffer interface, codecapi.iwmvideodecoderreconbuffersetreconstructedvideoframe, mf.iwmvideodecoderreconbuffersetreconstructedvideoframe, wmcodecdsp/IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame
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
 - IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame
 - wmcodecdsp/IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame
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
 - IWMVideoDecoderReconBuffer.SetReconstructedVideoFrame
---

# IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame


## -description

<div class="alert"><b>Note</b>  This method is obsolete and should not be used.</div>
<div> </div>
Restores the current reconstructed video frame.

## -parameters

### -param pBuf [in]

Address of an IMediaBuffer interface containing the reconstructed frame to restore.

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



<a href="/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmvideodecoderreconbuffer-getreconstructedvideoframesize">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize</a>