---
UID: NF:control.IVideoWindow.get_Width
title: IVideoWindow::get_Width (control.h)
author: windows-sdk-content
description: The get_Width method retrieves the width of the video window.
old-location: dshow\ivideowindow_get_width.htm
tech.root: DirectShow
ms.assetid: 179b065a-7269-40fa-8772-b336f27d69de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Width method, IVideoWindow.get_Width, IVideoWindow::get_Width, IVideoWindowget_Width, control/IVideoWindow::get_Width, dshow.ivideowindow_get_width, get_Width, get_Width method [DirectShow], get_Width method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_Width
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_Width


## -description



The <code>get_Width</code> method retrieves the width of the video window.




## -parameters




### -param pWidth [out]

Receives the width, in pixels.
          


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



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377327(v=VS.85).aspx">IVideoWindow::put_Width</a>
 

 

