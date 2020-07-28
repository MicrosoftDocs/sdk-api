---
UID: NF:control.IVideoWindow.put_Height
title: IVideoWindow::put_Height (control.h)
description: The put_Height method sets the height of the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_Height method","IVideoWindow.put_Height","IVideoWindow::put_Height","IVideoWindowput_Height","control/IVideoWindow::put_Height","dshow.ivideowindow_put_height","put_Height","put_Height method [DirectShow]","put_Height method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_height.htm
tech.root: dshow
ms.assetid: 39ba411f-675f-4dad-be4f-6beffbd3b53c
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Height method, IVideoWindow.put_Height, IVideoWindow::put_Height, IVideoWindowput_Height, control/IVideoWindow::put_Height, dshow.ivideowindow_put_height, put_Height, put_Height method [DirectShow], put_Height method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.put_Height
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
- IVideoWindow.put_Height
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::put_Height


## -description



The <code>put_Height</code> method sets the height of the video window.




## -parameters




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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_height">IVideoWindow::get_Height</a>
 

 

