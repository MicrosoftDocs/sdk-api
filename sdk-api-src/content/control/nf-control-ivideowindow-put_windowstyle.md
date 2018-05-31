---
UID: NF:control.IVideoWindow.put_WindowStyle
title: IVideoWindow::put_WindowStyle
author: windows-sdk-content
description: The put_WindowStyle method sets the window styles on the video window.
old-location: dshow\ivideowindow_put_windowstyle.htm
old-project: DirectShow
ms.assetid: cd1422d1-16a3-4aae-aadb-772a06173ba3
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoWindow interface [DirectShow],put_WindowStyle method, IVideoWindow.put_WindowStyle, IVideoWindow::put_WindowStyle, IVideoWindowput_WindowStyle, control/IVideoWindow::put_WindowStyle, dshow.ivideowindow_put_windowstyle, put_WindowStyle, put_WindowStyle method [DirectShow], put_WindowStyle method [DirectShow],IVideoWindow interface
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVideoWindow.put_WindowStyle
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::put_WindowStyle


## -description



The <code>put_WindowStyle</code> method sets the window styles on the video window.




## -parameters




### -param WindowStyle [in]

One or more flags from the GWL_STYLE value of the Windows <b>SetWindowLong</b> function.


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



This method is a thin wrapper over the <b>SetWindowLong</b> function and must be treated with care. In particular, you should retrieve the current styles and then add or remove flags. With some exceptions, flags allowed by the Windows <b>CreateWindow</b> function are acceptable. However, do not use this method to change the window size, and do not use the following flags:

<ul>
<li>WS_DISABLED</li>
<li>WS_HSCROLL</li>
<li>WS_ICONIC</li>
<li>WS_MAXIMIZE</li>
<li>WS_MINIMIZE</li>
<li>WS_VSCROLL</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/ae4ae516-743f-4a27-90d5-108ca26aadd4">IVideoWindow::get_WindowStyle</a>



<a href="https://msdn.microsoft.com/19d56e9d-6f6d-46aa-b46f-a62302b41d2f">IVideoWindow::put_WindowStyleEx</a>
 

 

