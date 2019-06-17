---
UID: NF:control.IVideoWindow.get_Top
title: IVideoWindow::get_Top (control.h)
author: windows-sdk-content
description: The get_Top method retrieves the video window's y-coordinate.
old-location: dshow\ivideowindow_get_top.htm
tech.root: DirectShow
ms.assetid: 00baab45-d740-4f74-bd53-eb2ff21c5dcc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Top method, IVideoWindow.get_Top, IVideoWindow::get_Top, IVideoWindowget_Top, control/IVideoWindow::get_Top, dshow.ivideowindow_get_top, get_Top, get_Top method [DirectShow], get_Top method [DirectShow],IVideoWindow interface
ms.topic: method
f1_keywords: ["control/IVideoWindow.get_Top"]
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
 - IVideoWindow.get_Top
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::get_Top


## -description



The <code>get_Top</code> method retrieves the video window's y-coordinate.




## -parameters




### -param pTop [out]

Receives the y-coordinate, in pixels.
          


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



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_top">IVideoWindow::put_Top</a>
 

 

