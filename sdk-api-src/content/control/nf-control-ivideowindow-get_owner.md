---
UID: NF:control.IVideoWindow.get_Owner
title: IVideoWindow::get_Owner
author: windows-sdk-content
description: The get_Owner method retrieves the video window's parent window, if any.
old-location: dshow\ivideowindow_get_owner.htm
old-project: DirectShow
ms.assetid: 9bb21c2a-25c6-43fa-a1b0-9f09944f1326
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Owner method, IVideoWindow.get_Owner, IVideoWindow::get_Owner, IVideoWindowget_Owner, control/IVideoWindow::get_Owner, dshow.ivideowindow_get_owner, get_Owner, get_Owner method [DirectShow], get_Owner method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_Owner
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_Owner


## -description



The <code>get_Owner</code> method retrieves the video window's parent window, if any.




## -parameters




### -param Owner






#### - pOwner [out]


            Receives a handle to the window, as an <a href="https://msdn.microsoft.com/80194b19-9c24-48f5-aca6-6ab33bd88c90">OAHWND</a> type. If the video window has no parent, this parameter receives the value <b>NULL</b>.
          


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
 

 

