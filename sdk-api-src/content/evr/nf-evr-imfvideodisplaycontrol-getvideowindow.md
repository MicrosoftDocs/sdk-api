---
UID: NF:evr.IMFVideoDisplayControl.GetVideoWindow
title: IMFVideoDisplayControl::GetVideoWindow (evr.h)

description: Gets the clipping window for the video.
old-location: mf\imfvideodisplaycontrol_getvideowindow.htm
tech.root: medfound
ms.assetid: 0b2b6b61-a2c5-4efd-ac40-962b0c2ae9c5

ms.date: 12/05/2018
ms.keywords: 0b2b6b61-a2c5-4efd-ac40-962b0c2ae9c5, GetVideoWindow, GetVideoWindow method [Media Foundation], GetVideoWindow method [Media Foundation],IMFVideoDisplayControl interface, IMFVideoDisplayControl interface [Media Foundation],GetVideoWindow method, IMFVideoDisplayControl.GetVideoWindow, IMFVideoDisplayControl::GetVideoWindow, evr/IMFVideoDisplayControl::GetVideoWindow, mf.imfvideodisplaycontrol_getvideowindow
ms.topic: method
f1_keywords: 
 - "evr/IMFVideoDisplayControl.GetVideoWindow"
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
 - IMFVideoDisplayControl.GetVideoWindow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl::GetVideoWindow


## -description


Gets the clipping window for the video.
        


## -parameters




### -param phwndVideo [out]

Receives a handle to the window where the enhanced video renderer (EVR) will draw the video.


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



There is no default clipping window. The application must set the clipping window.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

