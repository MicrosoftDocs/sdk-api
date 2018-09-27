---
UID: NF:control.IVideoWindow.put_Top
title: IVideoWindow::put_Top
author: windows-sdk-content
description: The put_Top method specifies the y-coordinate of the video window.
old-location: dshow\ivideowindow_put_top.htm
tech.root: DirectShow
ms.assetid: 1a5df1f1-3867-4956-8e1b-090aa8d8ff3a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Top method, IVideoWindow.put_Top, IVideoWindow::put_Top, IVideoWindowput_Top, control/IVideoWindow::put_Top, dshow.ivideowindow_put_top, put_Top, put_Top method [DirectShow], put_Top method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_Top
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377299(v=VS.85).aspx">IVideoWindow::get_Top</a>
 

 

