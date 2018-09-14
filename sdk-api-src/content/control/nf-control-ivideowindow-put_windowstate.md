---
UID: NF:control.IVideoWindow.put_WindowState
title: IVideoWindow::put_WindowState
author: windows-sdk-content
description: The put_WindowState method shows, hides, minimizes, or maximizes the video window.
old-location: dshow\ivideowindow_put_windowstate.htm
tech.root: DirectShow
ms.assetid: 75189754-61c4-4196-9cfb-3f8c8e33efbc
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IVideoWindow interface [DirectShow],put_WindowState method, IVideoWindow.put_WindowState, IVideoWindow::put_WindowState, IVideoWindowput_WindowState, control/IVideoWindow::put_WindowState, dshow.ivideowindow_put_windowstate, put_WindowState, put_WindowState method [DirectShow], put_WindowState method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_WindowState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::put_WindowState


## -description



The <code>put_WindowState</code> method shows, hides, minimizes, or maximizes the video window.




## -parameters




### -param WindowState [in]

Flag that specifies how the window is to be shown. The value can be any constant defined for the <i>nCmdShow</i> parameter of the <a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a> function. 


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377302(v=VS.85).aspx">IVideoWindow::get_WindowState</a>
 

 

