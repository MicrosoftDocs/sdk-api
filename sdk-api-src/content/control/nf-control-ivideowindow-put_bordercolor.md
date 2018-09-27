---
UID: NF:control.IVideoWindow.put_BorderColor
title: IVideoWindow::put_BorderColor
author: windows-sdk-content
description: The put_BorderColor method sets the color that appears around the edges of the destination rectangle.
old-location: dshow\ivideowindow_put_bordercolor.htm
tech.root: DirectShow
ms.assetid: c0e249f4-4a17-4c5d-8f16-bb1aceef2064
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVideoWindow interface [DirectShow],put_BorderColor method, IVideoWindow.put_BorderColor, IVideoWindow::put_BorderColor, IVideoWindowput_BorderColor, control/IVideoWindow::put_BorderColor, dshow.ivideowindow_put_bordercolor, put_BorderColor, put_BorderColor method [DirectShow], put_BorderColor method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_BorderColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::put_BorderColor


## -description



The <code>put_BorderColor</code> method sets the color that appears around the edges of the destination rectangle.




## -parameters




### -param Color [in]

The border color, specified as a <b>COLORREF</b> value.
          


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
 




## -remarks



If the destination rectangle is smaller than the client area of the video window, a border is exposed around the edges of the video. The default color is black. Use this method to override the default color. If a palette is in use, a nonsystem color is converted to its closest match.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd389600(v=VS.85).aspx">IBasicVideo::SetDestinationPosition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377292(v=VS.85).aspx">IVideoWindow::get_BorderColor</a>
 

 

