---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/e2a4600e-3d55-42f1-804c-8dc5bdf5daec">IWMVideoDecoderReconBuffer Interface</a>



<a href="https://msdn.microsoft.com/6e952923-2043-4b0d-b936-c570373a3544">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrame</a>



<a href="https://msdn.microsoft.com/7faadeed-4c89-4b3e-8e08-51de66224aaa">IWMVideoDecoderReconBuffer::GetReconstructedVideoFrameSize</a>
 

 

