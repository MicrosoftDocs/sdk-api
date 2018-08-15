---
UID: NF:control.IVideoWindow.get_BorderColor
title: IVideoWindow::get_BorderColor
author: windows-sdk-content
description: The get_BorderColor method retrieves the color that appears around the edges of the destination rectangle.
old-location: dshow\ivideowindow_get_bordercolor.htm
old-project: DirectShow
ms.assetid: 2f2df219-6b82-41fa-b0a9-251cc54fe019
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVideoWindow interface [DirectShow],get_BorderColor method, IVideoWindow.get_BorderColor, IVideoWindow::get_BorderColor, IVideoWindowget_BorderColor, control/IVideoWindow::get_BorderColor, dshow.ivideowindow_get_bordercolor, get_BorderColor, get_BorderColor method [DirectShow], get_BorderColor method [DirectShow],IVideoWindow interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.get_BorderColor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_BorderColor


## -description



The <code>get_BorderColor</code> method retrieves the color that appears around the edges of the destination rectangle.




## -parameters




### -param Color






#### - pColor [out]

Receives a <b>COLORREF</b> value.
          


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/c0e249f4-4a17-4c5d-8f16-bb1aceef2064">IVideoWindow::put_BorderColor</a>
 

 

