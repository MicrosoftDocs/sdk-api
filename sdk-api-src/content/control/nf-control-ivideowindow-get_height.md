---
UID: NF:control.IVideoWindow.get_Height
title: IVideoWindow::get_Height
author: windows-driver-content
description: The get_Height method retrieves the height of the video window.
old-location: dshow\ivideowindow_get_height.htm
old-project: DirectShow
ms.assetid: c1d29cd5-1e82-4406-b007-aa7b581d158e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Height method, IVideoWindow.get_Height, IVideoWindow::get_Height, IVideoWindowget_Height, control/IVideoWindow::get_Height, dshow.ivideowindow_get_height, get_Height, get_Height method [DirectShow], get_Height method [DirectShow],IVideoWindow interface
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
-	IVideoWindow.get_Height
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_Height


## -description



The <code>get_Height</code> method retrieves the height of the video window.




## -parameters




### -param pHeight [out]


            Receives the height, in pixels.
          


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



<a href="https://msdn.microsoft.com/39ba411f-675f-4dad-be4f-6beffbd3b53c">IVideoWindow::put_Height</a>
 

 

