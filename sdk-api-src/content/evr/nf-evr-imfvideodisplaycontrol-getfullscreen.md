---
UID: NF:evr.IMFVideoDisplayControl.GetFullscreen
title: IMFVideoDisplayControl::GetFullscreen (evr.h)
description: Queries whether the enhanced video renderer (EVR) is currently in full-screen mode.helpviewer_keywords: ["GetFullscreen","GetFullscreen method [Media Foundation]","GetFullscreen method [Media Foundation]","IMFVideoDisplayControl interface","IMFVideoDisplayControl interface [Media Foundation]","GetFullscreen method","IMFVideoDisplayControl.GetFullscreen","IMFVideoDisplayControl::GetFullscreen","ee564655-be8a-46f7-9682-acf3b38d056a","evr/IMFVideoDisplayControl::GetFullscreen","mf.imfvideodisplaycontrol_getfullscreen"]
old-location: mf\imfvideodisplaycontrol_getfullscreen.htm
tech.root: medfound
ms.assetid: ee564655-be8a-46f7-9682-acf3b38d056a
ms.date: 12/05/2018
ms.keywords: GetFullscreen, GetFullscreen method [Media Foundation], GetFullscreen method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetFullscreen method, IMFVideoDisplayControl.GetFullscreen, IMFVideoDisplayControl::GetFullscreen, ee564655-be8a-46f7-9682-acf3b38d056a, evr/IMFVideoDisplayControl::GetFullscreen, mf.imfvideodisplaycontrol_getfullscreen
f1_keywords:
- evr/IMFVideoDisplayControl.GetFullscreen
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
- IMFVideoDisplayControl.GetFullscreen
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::GetFullscreen


## -description


Queries whether the enhanced video renderer (EVR) is currently in full-screen mode.
        


## -parameters




### -param pfFullscreen [out]

Receives a Boolean value. If <b>TRUE</b>, the EVR is in full-screen mode. If <b>FALSE</b>, the EVR will display the video inside the application-provided clipping window.


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
The EVR is currently switching between full-screen and windowed mode.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

