---
UID: NF:evr.IMFVideoDisplayControl.SetVideoWindow
title: IMFVideoDisplayControl::SetVideoWindow
author: windows-sdk-content
description: Sets the clipping window for the video.
old-location: mf\imfvideodisplaycontrol_setvideowindow.htm
tech.root: medfound
ms.assetid: 50bc345c-ee44-4174-9b1a-e406041096b5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 50bc345c-ee44-4174-9b1a-e406041096b5, IMFVideoDisplayControl interface [Media Foundation],SetVideoWindow method, IMFVideoDisplayControl.SetVideoWindow, IMFVideoDisplayControl::SetVideoWindow, SetVideoWindow, SetVideoWindow method [Media Foundation], SetVideoWindow method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetVideoWindow, mf.imfvideodisplaycontrol_setvideowindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFVideoDisplayControl.SetVideoWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoDisplayControl::SetVideoWindow


## -description



Sets the clipping window for the video.




## -parameters




### -param hwndVideo [in]

Handle to the window where the enhanced video renderer (EVR) will draw the video.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>hwndVideo</i> does not specify a valid window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
DWM thumbnails were not enabled/disabled.

</td>
</tr>
</table>
 




## -remarks



The EVR will not display any video unless the application calls this method with a valid window handle.

For protected content, this method might disable Desktop Window Manager (DWM) thumbnail previews for the window. If thumbnail previews cannot be disabled, the method returns S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

