---
UID: NF:wmcodecdsp.IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame
title: IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame
author: windows-sdk-content
description: Note  This method is obsolete and should not be used. Retrieves the current reconstructed video frame.
old-location: mf\iwmvideodecoderreconbuffergetreconstructedvideoframe.htm
tech.root: medfound
ms.assetid: 6e952923-2043-4b0d-b936-c570373a3544
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetReconstructedVideoFrame, GetReconstructedVideoFrame method [Media Foundation], GetReconstructedVideoFrame method [Media Foundation],IWMVideoDecoderReconBuffer interface, IWMVideoDecoderReconBuffer interface [Media Foundation],GetReconstructedVideoFrame method, IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame, IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame, codecapi.iwmvideodecoderreconbuffergetreconstructedvideoframe, mf.iwmvideodecoderreconbuffergetreconstructedvideoframe, wmcodecdsp/IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame
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
 - IWMVideoDecoderReconBuffer.GetReconstructedVideoFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/e2a4600e-3d55-42f1-804c-8dc5bdf5daec">IWMVideoDecoderReconBuffer Interface</a>



<a href="https://msdn.microsoft.com/7faadeed-4c89-4b3e-8e08-51de66224aaa">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize</a>



<a href="https://msdn.microsoft.com/baffb56f-b2c5-464f-a2ae-1cb9677b8b83">IWMVideoDecoderReconBuffer::SetReconstructedVideoFrame</a>
 

 

