---
UID: NF:control.IVideoWindow.get_WindowState
title: IVideoWindow::get_WindowState
author: windows-sdk-content
description: The get_WindowState method queries whether the video window is visible, hidden, minimized, or maximized.
old-location: dshow\ivideowindow_get_windowstate.htm
tech.root: DirectShow
ms.assetid: ecda497c-634b-4a7e-9f21-85bde307c796
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVideoWindow interface [DirectShow],get_WindowState method, IVideoWindow.get_WindowState, IVideoWindow::get_WindowState, IVideoWindowget_WindowState, control/IVideoWindow::get_WindowState, dshow.ivideowindow_get_windowstate, get_WindowState, get_WindowState method [DirectShow], get_WindowState method [DirectShow],IVideoWindow interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IVideoWindow.get_WindowState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IVideoWindow.get_WindowState
: 
---

# IVideoWindow::get_WindowState


## -description



The <code>get_WindowState</code> method queries whether the video window is visible, hidden, minimized, or maximized.




## -parameters




### -param WindowState [out]

Receives one of the following flags:

<ul>
<li>SW_HIDE</li>
<li>SW_MAXIMIZE</li>
<li>SW_MINIMIZE</li>
<li>SW_SHOW</li>
</ul>
The meanings of these flags are defined by the Windows <b>ShowWindow</b> function.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/75189754-61c4-4196-9cfb-3f8c8e33efbc">IVideoWindow::put_WindowState</a>
 

 

