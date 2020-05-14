---
UID: NF:control.IVideoWindow.get_Left
title: IVideoWindow::get_Left (control.h)
description: The get_Left method retrieves the video window's x-axis coordinate.helpviewer_keywords: ["IVideoWindow interface [DirectShow]","get_Left method","IVideoWindow.get_Left","IVideoWindow::get_Left","IVideoWindowget_Left","control/IVideoWindow::get_Left","dshow.ivideowindow_get_left","get_Left","get_Left method [DirectShow]","get_Left method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_get_left.htm
tech.root: DirectShow
ms.assetid: 6d75c926-588c-4fb2-b537-f27602799b2e
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Left method, IVideoWindow.get_Left, IVideoWindow::get_Left, IVideoWindowget_Left, control/IVideoWindow::get_Left, dshow.ivideowindow_get_left, get_Left, get_Left method [DirectShow], get_Left method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.get_Left
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
- IVideoWindow.get_Left
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::get_Left


## -description



The <code>get_Left</code> method retrieves the video window's x-axis coordinate.




## -parameters




### -param pLeft [out]

Receives the x-axis coordinate, in pixels.
          


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



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_left">IVideoWindow::put_Left</a>
 

 

