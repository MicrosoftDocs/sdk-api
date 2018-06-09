---
UID: NF:control.IVideoWindow.put_Left
title: IVideoWindow::put_Left
author: windows-sdk-content
description: The put_Left method sets the x-coordinate of the video window.
old-location: dshow\ivideowindow_put_left.htm
old-project: DirectShow
ms.assetid: a614ee46-49cf-40e4-a1f7-b3b3b7065175
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Left method, IVideoWindow.put_Left, IVideoWindow::put_Left, IVideoWindowput_Left, control/IVideoWindow::put_Left, dshow.ivideowindow_put_left, put_Left, put_Left method [DirectShow], put_Left method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_Left
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/6d75c926-588c-4fb2-b537-f27602799b2e">IVideoWindow::get_Left</a>
 

 

