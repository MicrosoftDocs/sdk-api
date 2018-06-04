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

# IVideoWindow::put_MessageDrain


## -description



The <code>put_MessageDrain</code> method specifies a window to receive mouse and keyboard messages from the video window.




## -parameters




### -param Drain [in]


            A handle to the window, as an <a href="https://msdn.microsoft.com/80194b19-9c24-48f5-aca6-6ab33bd88c90">OAHWND</a> value.
          


## -returns



Possible return values include the following:

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer filter is not connected.

</td>
</tr>
</table>
 




## -remarks



This method enables an application to respond to mouse and keyboard events generated within the video window.

If <i>Drain</i> is non-<b>NULL</b>, the video renderer forwards certain messages to the specified window, using the <b>PostMessage</b> function. Which messages are forwarded might depend on the video renderer in use. The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> and Video Mixing Renderer (VMR) filters forward the following messages:

<ul>
<li>WM_CHAR</li>
<li>WM_DEADCHAR</li>
<li>WM_KEYDOWN</li>
<li>WM_KEYUP</li>
<li>WM_LBUTTONDBLCLK</li>
<li>WM_LBUTTONDOWN</li>
<li>WM_LBUTTONUP</li>
<li>WM_MBUTTONDBLCLK</li>
<li>WM_MBUTTONDOWN</li>
<li>WM_MBUTTONUP</li>
<li>WM_MOUSEACTIVATE</li>
<li>WM_MOUSEMOVE</li>
<li>WM_NCLBUTTONDBLCLK</li>
<li>WM_NCLBUTTONDOWN</li>
<li>WM_NCLBUTTONUP</li>
<li>WM_NCMBUTTONDBLCLK</li>
<li>WM_NCMBUTTONDOWN</li>
<li>WM_NCMBUTTONUP</li>
<li>WM_NCMOUSEMOVE</li>
<li>WM_NCRBUTTONDBLCLK</li>
<li>WM_NCRBUTTONDOWN</li>
<li>WM_NCRBUTTONUP</li>
<li>WM_RBUTTONDBLCLK</li>
<li>WM_RBUTTONDOWN</li>
<li>WM_RBUTTONUP</li>
<li>WM_SYSCHAR</li>
<li>WM_SYSDEADCHAR</li>
<li>WM_SYSKEYDOWN</li>
<li>WM_SYSKEYUP</li>
</ul>
The message drain window does not need to be a parent of the video window, so full-screen applications can use this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/9a1a3070-5b68-4dd2-bc10-97a8331cc262">IVideoWindow::get_MessageDrain</a>
 

 

