---
UID: NF:evr.IMFVideoDisplayControl.RepaintVideo
title: IMFVideoDisplayControl::RepaintVideo
author: windows-sdk-content
description: Repaints the current video frame. Call this method whenever the application receives a WM_PAINT message.
old-location: mf\imfvideodisplaycontrol_repaintvideo.htm
old-project: medfound
ms.assetid: c8051883-2a48-4ca4-a7d2-c90d0d451cd2
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFVideoDisplayControl interface [Media Foundation],RepaintVideo method, IMFVideoDisplayControl.RepaintVideo, IMFVideoDisplayControl::RepaintVideo, RepaintVideo, RepaintVideo method [Media Foundation], RepaintVideo method [Media Foundation],IMFVideoDisplayControl interface, c8051883-2a48-4ca4-a7d2-c90d0d451cd2, evr/IMFVideoDisplayControl::RepaintVideo, mf.imfvideodisplaycontrol_repaintvideo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: evr.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFVideoMixPrefs
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

