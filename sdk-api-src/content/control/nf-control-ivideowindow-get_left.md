---
UID: NF:control.IVideoWindow.get_Left
title: IVideoWindow::get_Left method
author: windows-driver-content
description: The get_Left method retrieves the video window's x-axis coordinate.
old-location: dshow\ivideowindow_get_left.htm
old-project: DirectShow
ms.assetid: 6d75c926-588c-4fb2-b537-f27602799b2e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVideoWindow, IVideoWindow interface [DirectShow], get_Left method, IVideoWindow::get_Left, IVideoWindowget_Left, control/IVideoWindow::get_Left, dshow.ivideowindow_get_left, get_Left method [DirectShow], get_Left method [DirectShow], IVideoWindow interface, get_Left,IVideoWindow.get_Left
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
-	IVideoWindow.get_Left
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_Left method


## -description



The <code>get_Left</code> method retrieves the video window's x-axis coordinate.




## -parameters




### -param pLeft [out]

Receives the x-axis coordinate, in pixels.
          


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



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/a614ee46-49cf-40e4-a1f7-b3b3b7065175">IVideoWindow::put_Left</a>
 

 

