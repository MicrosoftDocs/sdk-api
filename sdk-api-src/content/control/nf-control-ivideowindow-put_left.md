---
UID: NF:control.IVideoWindow.put_Left
title: IVideoWindow::put_Left
author: windows-sdk-content
description: The put_Left method sets the x-coordinate of the video window.
old-location: dshow\ivideowindow_put_left.htm
tech.root: DirectShow
ms.assetid: a614ee46-49cf-40e4-a1f7-b3b3b7065175
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Left method, IVideoWindow.put_Left, IVideoWindow::put_Left, IVideoWindowput_Left, control/IVideoWindow::put_Left, dshow.ivideowindow_put_left, put_Left, put_Left method [DirectShow], put_Left method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_Left
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IVideoWindow.put_Left
: 
---

# IVideoWindow::put_Left


## -description



The <code>put_Left</code> method sets the x-coordinate of the video window.




## -parameters




### -param Left [in]

The x-coordinate, in pixels.
          


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



<a href="https://msdn.microsoft.com/en-us/library/Dd377296(v=VS.85).aspx">IVideoWindow::get_Left</a>
 

 

