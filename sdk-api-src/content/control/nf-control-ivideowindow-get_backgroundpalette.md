---
UID: NF:control.IVideoWindow.get_BackgroundPalette
title: IVideoWindow::get_BackgroundPalette (control.h)
description: The get_BackgroundPalette method queries whether the video window realizes its palette in the background..helpviewer_keywords: ["IVideoWindow interface [DirectShow]","get_BackgroundPalette method","IVideoWindow.get_BackgroundPalette","IVideoWindow::get_BackgroundPalette","IVideoWindowget_BackgroundPalette","control/IVideoWindow::get_BackgroundPalette","dshow.ivideowindow_get_backgroundpalette","get_BackgroundPalette","get_BackgroundPalette method [DirectShow]","get_BackgroundPalette method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_get_backgroundpalette.htm
tech.root: DirectShow
ms.assetid: cdd11f60-e042-4aad-a867-d1e12a88ebfe
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],get_BackgroundPalette method, IVideoWindow.get_BackgroundPalette, IVideoWindow::get_BackgroundPalette, IVideoWindowget_BackgroundPalette, control/IVideoWindow::get_BackgroundPalette, dshow.ivideowindow_get_backgroundpalette, get_BackgroundPalette, get_BackgroundPalette method [DirectShow], get_BackgroundPalette method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.get_BackgroundPalette
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
- IVideoWindow.get_BackgroundPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::get_BackgroundPalette


## -description



The <code>get_BackgroundPalette</code> method queries whether the video window realizes its palette in the background..




## -parameters




### -param pBackgroundPalette [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE
                </td>
<td>The video window realizes the palette in the background.</td>
</tr>
<tr>
<td>OAFALSE
                </td>
<td>The video window does not realize the palette in the background.</td>
</tr>
</table>
 


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



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_backgroundpalette">IVideoWindow::put_BackgroundPalette</a>
 

 

