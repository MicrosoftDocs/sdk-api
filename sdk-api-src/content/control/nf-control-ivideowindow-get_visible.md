---
UID: NF:control.IVideoWindow.get_Visible
title: IVideoWindow::get_Visible (control.h)
author: windows-sdk-content
description: The get_Visible method queries whether the video window is visible.
old-location: dshow\ivideowindow_get_visible.htm
tech.root: DirectShow
ms.assetid: b533398e-80f6-4f33-982b-93b8e0d705e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Visible method, IVideoWindow.get_Visible, IVideoWindow::get_Visible, IVideoWindowget_Visible, control/IVideoWindow::get_Visible, dshow.ivideowindow_get_visible, get_Visible, get_Visible method [DirectShow], get_Visible method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_Visible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_Visible


## -description



The <code>get_Visible</code> method queries whether the video window is visible.




## -parameters




### -param pVisible [out]

Receives the value OATRUE if the window is visible, or OAFALSE if the window is hidden.
          


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
 




## -remarks



This method checks for the WS_VISIBLE style bit, by calling the Windows <b>IsWindowVisible</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377326(v=VS.85).aspx">IVideoWindow::put_Visible</a>
 

 

