---
UID: NF:evr.IMFVideoDisplayControl.SetFullscreen
title: IMFVideoDisplayControl::SetFullscreen
author: windows-sdk-content
description: Sets or unsets full-screen rendering mode.
old-location: mf\imfvideodisplaycontrol_setfullscreen.htm
tech.root: medfound
ms.assetid: 95c85fb2-9267-477f-aa47-1c050ccc1bdd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 95c85fb2-9267-477f-aa47-1c050ccc1bdd, IMFVideoDisplayControl interface [Media Foundation],SetFullscreen method, IMFVideoDisplayControl.SetFullscreen, IMFVideoDisplayControl::SetFullscreen, SetFullscreen, SetFullscreen method [Media Foundation], SetFullscreen method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetFullscreen, mf.imfvideodisplaycontrol_setfullscreen
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
 - IMFVideoDisplayControl.SetFullscreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoDisplayControl::SetFullscreen


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. ]

Sets or unsets full-screen rendering mode.

To implement full-screen playback, an application should simply resize the video window to cover the entire area of the monitor. Also set the window to be a topmost window, so that the application receives all mouse-click messages. For more information about topmost windows, see the documentation for the <a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a> function.


## -parameters




### -param fFullscreen [in]

If <b>TRUE</b>, the enhanced video renderer (EVR) uses full-screen mode. If <b>FALSE</b>, the EVR draws the video in the application-provided clipping window.
          


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



The default EVR presenter implements full-screen mode using Direct3D exclusive mode.
      

If you use this  method  to switch to full-screen mode, set the application window to be a topmost window and resize the window to cover the entire monitor. This ensures that the application window receives all mouse-click messages. Also set the keyboard focus to the application window. When you switch out of full-screen mode, restore the window's original size and position.
      

By default, the cursor is still visible in full-screen mode. To hide the cursor, call <b>ShowCursor</b>.
      

The transition to and from full-screen mode occurs asynchronously. To get the current mode, call <a href="https://msdn.microsoft.com/ee564655-be8a-46f7-9682-acf3b38d056a">IMFVideoDisplayControl::GetFullscreen</a>.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/db9b4663-9240-484f-8c47-cb1f5daa238d">IMFVideoDisplayControl</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

