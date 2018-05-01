---
UID: NF:control.IVideoWindow.get_Caption
title: IVideoWindow::get_Caption method
author: windows-driver-content
description: The get_Caption method retrieves the video window caption.
old-location: dshow\ivideowindow_get_caption.htm
old-project: DirectShow
ms.assetid: fbb42e55-1be1-4931-869b-9e8d4af5e6df
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVideoWindow, IVideoWindow interface [DirectShow], get_Caption method, IVideoWindow::get_Caption, IVideoWindowget_Caption, control/IVideoWindow::get_Caption, dshow.ivideowindow_get_caption, get_Caption method [DirectShow], get_Caption method [DirectShow], IVideoWindow interface, get_Caption,IVideoWindow.get_Caption
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
-	IVideoWindow.get_Caption
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_Caption method


## -description



The <code>get_Caption</code> method retrieves the video window caption.




## -parameters




### -param strCaption [out]

Pointer to a <b>BSTR</b> that receives the caption.


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



The caller must free the returned string, using the <b>SysFreeString</b> function.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/d16dca01-95ba-4573-b9c4-ab996dcf21e4">IVideoWindow::put_Caption</a>
 

 

