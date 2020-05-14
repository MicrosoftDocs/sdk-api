---
UID: NF:control.IVideoWindow.SetWindowPosition
title: IVideoWindow::SetWindowPosition (control.h)
description: The SetWindowPosition method sets the position of the video window.helpviewer_keywords: ["IVideoWindow interface [DirectShow]","SetWindowPosition method","IVideoWindow.SetWindowPosition","IVideoWindow::SetWindowPosition","IVideoWindowSetWindowPosition","SetWindowPosition","SetWindowPosition method [DirectShow]","SetWindowPosition method [DirectShow]","IVideoWindow interface","control/IVideoWindow::SetWindowPosition","dshow.ivideowindow_setwindowposition"]
old-location: dshow\ivideowindow_setwindowposition.htm
tech.root: DirectShow
ms.assetid: 5e667044-1781-4380-b855-d15cf8cd2349
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],SetWindowPosition method, IVideoWindow.SetWindowPosition, IVideoWindow::SetWindowPosition, IVideoWindowSetWindowPosition, SetWindowPosition, SetWindowPosition method [DirectShow], SetWindowPosition method [DirectShow],IVideoWindow interface, control/IVideoWindow::SetWindowPosition, dshow.ivideowindow_setwindowposition
f1_keywords:
- control/IVideoWindow.SetWindowPosition
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
- IVideoWindow.SetWindowPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::SetWindowPosition


## -description



The <code>SetWindowPosition</code> method sets the position of the video window.




## -parameters




### -param Left [in]

The x-coordinate, in pixels.
          


### -param Top [in]

The y-coordinate, in pixels.
          


### -param Width [in]

The width, in pixels.
          


### -param Height [in]

The height, in pixels.
          


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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



This method has the same effect as calling the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_left">IVideoWindow::put_Left</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_top">IVideoWindow::put_Top</a>, <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_width">IVideoWindow::put_Width</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_height">IVideoWindow::put_Height</a> methods.

If resizing the window to the specified dimensions is impossible, this method modifies the window's size and location to make the window fit. Call the <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-getwindowposition">IVideoWindow::GetWindowPosition</a> method to determine the result.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>
 

 

