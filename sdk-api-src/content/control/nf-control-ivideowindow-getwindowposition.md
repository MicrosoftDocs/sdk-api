---
UID: NF:control.IVideoWindow.GetWindowPosition
title: IVideoWindow::GetWindowPosition
author: windows-sdk-content
description: The GetWindowPosition method retrieves the position of the video window.
old-location: dshow\ivideowindow_getwindowposition.htm
tech.root: DirectShow
ms.assetid: df55c10d-aec1-42f3-8bfb-207ae8804e72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetWindowPosition, GetWindowPosition method [DirectShow], GetWindowPosition method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],GetWindowPosition method, IVideoWindow.GetWindowPosition, IVideoWindow::GetWindowPosition, IVideoWindowGetWindowPosition, control/IVideoWindow::GetWindowPosition, dshow.ivideowindow_getwindowposition
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
 - IVideoWindow.GetWindowPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::GetWindowPosition


## -description



The <code>GetWindowPosition</code> method retrieves the position of the video window.




## -parameters




### -param pLeft [out]

Receives the x-coordinate, in pixels.


### -param pTop [out]

Receives the y-coordinate, in pixels.


### -param pWidth [out]

Receives the width of the window, in pixels.
          


### -param pHeight [out]

Receives the height of the window, in pixels.
          


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
 




## -remarks



This method has the same effect as calling the <a href="https://msdn.microsoft.com/en-us/library/Dd377296(v=VS.85).aspx">IVideoWindow::get_Left</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd377299(v=VS.85).aspx">IVideoWindow::get_Top</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd377301(v=VS.85).aspx">IVideoWindow::get_Width</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd377295(v=VS.85).aspx">IVideoWindow::get_Height</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377334(v=VS.85).aspx">IVideoWindow::SetWindowPosition</a>
 

 

