---
UID: NF:evr.IMFVideoDisplayControl.GetBorderColor
title: IMFVideoDisplayControl::GetBorderColor (evr.h)
author: windows-sdk-content
description: Gets the border color for the video.
old-location: mf\imfvideodisplaycontrol_getbordercolor.htm
tech.root: medfound
ms.assetid: 1b65b793-d06d-4d7f-a19f-0068dd7f2e44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1b65b793-d06d-4d7f-a19f-0068dd7f2e44, GetBorderColor, GetBorderColor method [Media Foundation], GetBorderColor method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetBorderColor method, IMFVideoDisplayControl.GetBorderColor, IMFVideoDisplayControl::GetBorderColor, evr/IMFVideoDisplayControl::GetBorderColor, mf.imfvideodisplaycontrol_getbordercolor
ms.topic: method
f1_keywords: 
 - "evr/IMFVideoDisplayControl.GetBorderColor"
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.GetBorderColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::GetBorderColor


## -description


Gets the border color for the video.
        


## -parameters




### -param pClr [out]

Receives the border color, as a <b>COLORREF</b> value.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -remarks



The border color is used for areas where the enhanced video renderer (EVR) does not draw any video.

The border color is not used for letterboxing. To get the letterbox color, call <a href="https://docs.microsoft.com/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getbackgroundcolor">IMFVideoProcessor::GetBackgroundColor</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

