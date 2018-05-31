---
UID: NF:control.IVideoWindow.NotifyOwnerMessage
title: IVideoWindow::NotifyOwnerMessage
author: windows-sdk-content
description: The NotifyOwnerMessage method forwards a message to the video window.
old-location: dshow\ivideowindow_notifyownermessage.htm
old-project: DirectShow
ms.assetid: 37d28f32-5da5-4082-ac57-5b274e95ca68
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoWindow interface [DirectShow],NotifyOwnerMessage method, IVideoWindow.NotifyOwnerMessage, IVideoWindow::NotifyOwnerMessage, IVideoWindowNotifyOwnerMessage, NotifyOwnerMessage, NotifyOwnerMessage method [DirectShow], NotifyOwnerMessage method [DirectShow],IVideoWindow interface, control/IVideoWindow::NotifyOwnerMessage, dshow.ivideowindow_notifyownermessage
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
-	IVideoWindow.NotifyOwnerMessage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::NotifyOwnerMessage


## -description



The <code>NotifyOwnerMessage</code> method forwards a message to the video window.




## -parameters




### -param hwnd [in]


            A handle to the window, as an <a href="https://msdn.microsoft.com/80194b19-9c24-48f5-aca6-6ab33bd88c90">OAHWND</a> value.
          


### -param uMsg [in]

Specifies the message.


### -param wParam [in]

Message parameter.


### -param lParam [in]

Message parameter.


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



The Filter Graph Manager calls this method to pass various messages to the renderer, including the following:

<ul>
<li>WM_ACTIVATEAPP</li>
<li>WM_DEVMODECHANGE</li>
<li>WM_DISPLAYCHANGE</li>
<li>WM_PALETTECHANGED</li>
<li>WM_PALETTEISCHANGING</li>
<li>WM_QUERYNEWPALETTE</li>
<li>WM_SYSCOLORCHANGE</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>
 

 

