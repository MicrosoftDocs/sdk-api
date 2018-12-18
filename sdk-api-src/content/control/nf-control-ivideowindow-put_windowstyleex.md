---
UID: NF:control.IVideoWindow.put_WindowStyleEx
title: IVideoWindow::put_WindowStyleEx
author: windows-sdk-content
description: The put_WindowStyleEx method sets the extended window styles on the video window.
old-location: dshow\ivideowindow_put_windowstyleex.htm
tech.root: DirectShow
ms.assetid: 19d56e9d-6f6d-46aa-b46f-a62302b41d2f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoWindow interface [DirectShow],put_WindowStyleEx method, IVideoWindow.put_WindowStyleEx, IVideoWindow::put_WindowStyleEx, IVideoWindowput_WindowStyleEx, control/IVideoWindow::put_WindowStyleEx, dshow.ivideowindow_put_windowstyleex, put_WindowStyleEx, put_WindowStyleEx method [DirectShow], put_WindowStyleEx method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_WindowStyleEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::put_WindowStyleEx


## -description



The <code>put_WindowStyleEx</code> method sets the extended window styles on the video window.




## -parameters




### -param WindowStyleEx [in]

One or more flags from the GWL_EXSTYLE value of the Windows <b>SetWindowLong</b> function.


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



This method is a thin wrapper over the <b>SetWindowLong</b> function and must be treated with care. In particular, you should retrieve the current styles and then add or remove flags. With some exceptions, flags allowed by the Windows <b>CreateWindow</b> function are acceptable. However, do not use this method to change the window size.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377304(v=VS.85).aspx">IVideoWindow::get_WindowStyleEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377329(v=VS.85).aspx">IVideoWindow::put_WindowStyle</a>
 

 

