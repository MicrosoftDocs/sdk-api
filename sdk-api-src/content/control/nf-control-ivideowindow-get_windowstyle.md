---
UID: NF:control.IVideoWindow.get_WindowStyle
title: IVideoWindow::get_WindowStyle (control.h)
author: windows-sdk-content
description: The get_WindowStyle method retrieves the window styles on the video window.
old-location: dshow\ivideowindow_get_windowstyle.htm
tech.root: DirectShow
ms.assetid: ae4ae516-743f-4a27-90d5-108ca26aadd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],get_WindowStyle method, IVideoWindow.get_WindowStyle, IVideoWindow::get_WindowStyle, IVideoWindowget_WindowStyle, control/IVideoWindow::get_WindowStyle, dshow.ivideowindow_get_windowstyle, get_WindowStyle, get_WindowStyle method [DirectShow], get_WindowStyle method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_WindowStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_WindowStyle


## -description



The <code>get_WindowStyle</code> method retrieves the window styles on the video window.




## -parameters




### -param WindowStyle [out]

Receives the window style flags.
          


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



This method calls the Windows <b>GetWindowLong</b> function with the value GWL_STYLE.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377304(v=VS.85).aspx">IVideoWindow::get_WindowStyleEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377329(v=VS.85).aspx">IVideoWindow::put_WindowStyle</a>
 

 

