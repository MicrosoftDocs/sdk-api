---
UID: NF:control.IVideoWindow.put_Top
title: IVideoWindow::put_Top
author: windows-sdk-content
description: The put_Top method specifies the y-coordinate of the video window.
old-location: dshow\ivideowindow_put_top.htm
old-project: DirectShow
ms.assetid: 1a5df1f1-3867-4956-8e1b-090aa8d8ff3a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Top method, IVideoWindow.put_Top, IVideoWindow::put_Top, IVideoWindowput_Top, control/IVideoWindow::put_Top, dshow.ivideowindow_put_top, put_Top, put_Top method [DirectShow], put_Top method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_Top
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::put_Top


## -description



The <code>put_Top</code> method specifies the y-coordinate of the video window.




## -parameters




### -param Top [in]

The y-coordinate, in pixels.
          


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/00baab45-d740-4f74-bd53-eb2ff21c5dcc">IVideoWindow::get_Top</a>
 

 

