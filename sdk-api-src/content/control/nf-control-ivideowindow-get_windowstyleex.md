---
UID: NF:control.IVideoWindow.get_WindowStyleEx
title: IVideoWindow::get_WindowStyleEx
author: windows-sdk-content
description: The get_WindowStyleEx method retrieves the extended window styles on the video window.
old-location: dshow\ivideowindow_get_windowstyleex.htm
tech.root: DirectShow
ms.assetid: cdffe918-5802-406e-86b1-d1e9ebb6dbf7
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IVideoWindow interface [DirectShow],get_WindowStyleEx method, IVideoWindow.get_WindowStyleEx, IVideoWindow::get_WindowStyleEx, IVideoWindowget_WindowStyleEx, control/IVideoWindow::get_WindowStyleEx, dshow.ivideowindow_get_windowstyleex, get_WindowStyleEx, get_WindowStyleEx method [DirectShow], get_WindowStyleEx method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_WindowStyleEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_WindowStyleEx


## -description



The <code>get_WindowStyleEx</code> method retrieves the extended window styles on the video window.




## -parameters




### -param WindowStyleEx

TBD




#### - pWindowStyleEx [out, retval]

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



This method calls the Windows <b>GetWindowLong</b> function with the value GWL_EXSTYLE.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377303(v=VS.85).aspx">IVideoWindow::get_WindowStyle</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377330(v=VS.85).aspx">IVideoWindow::put_WindowStyleEx</a>
 

 

