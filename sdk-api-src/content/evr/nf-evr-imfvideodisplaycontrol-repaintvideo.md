---
UID: NF:evr.IMFVideoDisplayControl.RepaintVideo
title: IMFVideoDisplayControl::RepaintVideo (evr.h)
description: Repaints the current video frame. Call this method whenever the application receives a WM_PAINT message.
helpviewer_keywords: ["IMFVideoDisplayControl interface [Media Foundation]","RepaintVideo method","IMFVideoDisplayControl.RepaintVideo","IMFVideoDisplayControl::RepaintVideo","RepaintVideo","RepaintVideo method [Media Foundation]","RepaintVideo method [Media Foundation]","IMFVideoDisplayControl interface","c8051883-2a48-4ca4-a7d2-c90d0d451cd2","evr/IMFVideoDisplayControl::RepaintVideo","mf.imfvideodisplaycontrol_repaintvideo"]
old-location: mf\imfvideodisplaycontrol_repaintvideo.htm
tech.root: mf
ms.assetid: c8051883-2a48-4ca4-a7d2-c90d0d451cd2
ms.date: 12/05/2018
ms.keywords: IMFVideoDisplayControl interface [Media Foundation],RepaintVideo method, IMFVideoDisplayControl.RepaintVideo, IMFVideoDisplayControl::RepaintVideo, RepaintVideo, RepaintVideo method [Media Foundation], RepaintVideo method [Media Foundation],IMFVideoDisplayControl interface, c8051883-2a48-4ca4-a7d2-c90d0d451cd2, evr/IMFVideoDisplayControl::RepaintVideo, mf.imfvideodisplaycontrol_repaintvideo
f1_keywords:
- evr/IMFVideoDisplayControl.RepaintVideo
dev_langs:
- c++
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
- IMFVideoDisplayControl.RepaintVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::RepaintVideo


## -description



Repaints the current video frame. Call this method whenever the application receives a WM_PAINT message.




## -parameters






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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The EVR cannot repaint the frame at this time. This error can occur while the EVR is switching between full-screen and windowed mode. The caller can safely ignore this error.

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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

