---
UID: NF:control.IVideoWindow.get_WindowState
title: IVideoWindow::get_WindowState (control.h)
description: The get_WindowState method queries whether the video window is visible, hidden, minimized, or maximized.helpviewer_keywords: ["IVideoWindow interface [DirectShow]","get_WindowState method","IVideoWindow.get_WindowState","IVideoWindow::get_WindowState","IVideoWindowget_WindowState","control/IVideoWindow::get_WindowState","dshow.ivideowindow_get_windowstate","get_WindowState","get_WindowState method [DirectShow]","get_WindowState method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_get_windowstate.htm
tech.root: DirectShow
ms.assetid: ecda497c-634b-4a7e-9f21-85bde307c796
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],get_WindowState method, IVideoWindow.get_WindowState, IVideoWindow::get_WindowState, IVideoWindowget_WindowState, control/IVideoWindow::get_WindowState, dshow.ivideowindow_get_windowstate, get_WindowState, get_WindowState method [DirectShow], get_WindowState method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.get_WindowState
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_windowstate">IVideoWindow::put_WindowState</a>
 

 

