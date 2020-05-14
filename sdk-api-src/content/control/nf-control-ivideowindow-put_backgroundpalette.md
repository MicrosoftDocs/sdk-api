---
UID: NF:control.IVideoWindow.put_BackgroundPalette
title: IVideoWindow::put_BackgroundPalette (control.h)
description: The put_BackgroundPalette method specifies whether the video window realizes its palette in the background.helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_BackgroundPalette method","IVideoWindow.put_BackgroundPalette","IVideoWindow::put_BackgroundPalette","IVideoWindowput_BackgroundPalette","control/IVideoWindow::put_BackgroundPalette","dshow.ivideowindow_put_backgroundpalette","put_BackgroundPalette","put_BackgroundPalette method [DirectShow]","put_BackgroundPalette method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_backgroundpalette.htm
tech.root: DirectShow
ms.assetid: 0b1d34b6-0043-4929-a496-cf84b5d47b55
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],put_BackgroundPalette method, IVideoWindow.put_BackgroundPalette, IVideoWindow::put_BackgroundPalette, IVideoWindowput_BackgroundPalette, control/IVideoWindow::put_BackgroundPalette, dshow.ivideowindow_put_backgroundpalette, put_BackgroundPalette, put_BackgroundPalette method [DirectShow], put_BackgroundPalette method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.put_BackgroundPalette
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
- IVideoWindow.put_BackgroundPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::put_BackgroundPalette


## -description



The <code>put_BackgroundPalette</code> method specifies whether the video window realizes its palette in the background.




## -parameters




### -param BackgroundPalette [in]

Specifies whether the video renderer realizes it palette in the background. Must be one of the following values:

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
<td>The video renderer realizes the palette in the background.</td>
</tr>
<tr>
<td>OAFALSE
                </td>
<td>The video renderer does not realize the palette in the background. (Default.)</td>
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



If <i>BackgroundPalette</i> is <b>OATRUE</b> and the video image requires a pallette, the video renderer will realize that palette in the background. Any colors that the palette uses will change to their closest match in the display palette prior to drawing. This ensures that an application will not have its palette disturbed. However, it imposes severe performance penalties on the video.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_backgroundpalette">IVideoWindow::get_BackgroundPalette</a>
 

 

