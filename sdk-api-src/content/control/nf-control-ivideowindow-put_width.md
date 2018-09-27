---
UID: NF:control.IVideoWindow.put_Width
title: IVideoWindow::put_Width
author: windows-sdk-content
description: The put_Width method specifies the width of the video window.
old-location: dshow\ivideowindow_put_width.htm
tech.root: DirectShow
ms.assetid: 7cb02033-0405-4b8b-91fc-2f33097f2c88
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Width method, IVideoWindow.put_Width, IVideoWindow::put_Width, IVideoWindowput_Width, control/IVideoWindow::put_Width, dshow.ivideowindow_put_width, put_Width, put_Width method [DirectShow], put_Width method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_Width
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::put_Width


## -description



The <code>put_Width</code> method specifies the width of the video window.




## -parameters




### -param Width [in]

The width, in pixels.
          


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



<a href="https://msdn.microsoft.com/en-us/library/Dd377301(v=VS.85).aspx">IVideoWindow::get_Width</a>
 

 

