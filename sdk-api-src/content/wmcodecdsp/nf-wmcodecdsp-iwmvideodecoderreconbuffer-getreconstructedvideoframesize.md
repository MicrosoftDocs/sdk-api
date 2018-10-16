---
UID: NF:wmcodecdsp.IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize
title: IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize
author: windows-sdk-content
description: Note  This method is obsolete and should not be used. Retrieves the size of the current reconstructed video frame.
old-location: mf\iwmvideodecoderreconbuffergetreconstructedvideoframesize.htm
tech.root: medfound
ms.assetid: 7faadeed-4c89-4b3e-8e08-51de66224aaa
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetReconstructedVideoFrameSize, GetReconstructedVideoFrameSize method [Media Foundation], GetReconstructedVideoFrameSize method [Media Foundation],IWMVideoDecoderReconBuffer interface, IWMVideoDecoderReconBuffer interface [Media Foundation],GetReconstructedVideoFrameSize method, IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize, IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize, codecapi.iwmvideodecoderreconbuffergetreconstructedvideoframesize, mf.iwmvideodecoderreconbuffergetreconstructedvideoframesize, wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMVideoDecoderReconBuffer.GetReconstructedVideoFrameSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/e2a4600e-3d55-42f1-804c-8dc5bdf5daec">IWMVideoDecoderReconBuffer Interface</a>



<a href="https://msdn.microsoft.com/6e952923-2043-4b0d-b936-c570373a3544">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame</a>



<a href="https://msdn.microsoft.com/baffb56f-b2c5-464f-a2ae-1cb9677b8b83">IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame</a>
 

 

