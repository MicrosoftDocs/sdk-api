---
UID: NF:control.IVideoWindow.SetWindowForeground
title: IVideoWindow::SetWindowForeground
author: windows-driver-content
description: The SetWindowForeground method places the video window at the top of the Z order.
old-location: dshow\ivideowindow_setwindowforeground.htm
old-project: DirectShow
ms.assetid: ff4f3707-1f2e-499b-8108-81616fe4ae9b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IVideoWindow interface [DirectShow],SetWindowForeground method, IVideoWindow.SetWindowForeground, IVideoWindow::SetWindowForeground, IVideoWindowSetWindowForeground, SetWindowForeground, SetWindowForeground method [DirectShow], SetWindowForeground method [DirectShow],IVideoWindow interface, control/IVideoWindow::SetWindowForeground, dshow.ivideowindow_setwindowforeground
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
-	IVideoWindow.SetWindowForeground
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::SetWindowForeground


## -description



The <code>SetWindowForeground</code> method places the video window at the top of the Z order.




## -parameters




### -param Focus

Specifies whether to give the window focus. Must be one of the following values:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>
                  OATRUE
                </td>
<td>Give the window focus.</td>
</tr>
<tr>
<td>
                  OAFALSE
                </td>
<td>Do not give the window focus.</td>
</tr>
</table>
 


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
 

 

