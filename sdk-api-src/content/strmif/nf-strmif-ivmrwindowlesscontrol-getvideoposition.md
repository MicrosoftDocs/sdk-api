---
UID: NF:strmif.IVMRWindowlessControl.GetVideoPosition
title: IVMRWindowlessControl::GetVideoPosition (strmif.h)
author: windows-sdk-content
description: The GetVideoPosition method retrieves the current source and destination rectangles used to display the video.
old-location: dshow\ivmrwindowlesscontrol_getvideoposition.htm
tech.root: DirectShow
ms.assetid: 1d7f1a8b-bbc4-43ae-b8e6-410561087204
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVideoPosition, GetVideoPosition method [DirectShow], GetVideoPosition method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetVideoPosition method, IVMRWindowlessControl.GetVideoPosition, IVMRWindowlessControl::GetVideoPosition, IVMRWindowlessControlGetVideoPosition, dshow.ivmrwindowlesscontrol_getvideoposition, strmif/IVMRWindowlessControl::GetVideoPosition
ms.topic: method
f1_keywords: 
 - "strmif/IVMRWindowlessControl.GetVideoPosition"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRWindowlessControl.GetVideoPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::GetVideoPosition


## -description



The <code>GetVideoPosition</code> method retrieves the current source and destination rectangles used to display the video.




## -parameters




### -param lpSRCRect [out]

Pointer that receives the current source rectangle.


### -param lpDSTRect [out]

Pointer that receives the current destination rectangle.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition">IVMRWindowlessControl::SetVideoPosition</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

