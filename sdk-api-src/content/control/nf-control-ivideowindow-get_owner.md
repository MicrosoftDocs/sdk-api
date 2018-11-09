---
UID: NF:control.IVideoWindow.get_Owner
title: IVideoWindow::get_Owner
author: windows-sdk-content
description: The get_Owner method retrieves the video window's parent window, if any.
old-location: dshow\ivideowindow_get_owner.htm
tech.root: DirectShow
ms.assetid: 9bb21c2a-25c6-43fa-a1b0-9f09944f1326
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Owner method, IVideoWindow.get_Owner, IVideoWindow::get_Owner, IVideoWindowget_Owner, control/IVideoWindow::get_Owner, dshow.ivideowindow_get_owner, get_Owner, get_Owner method [DirectShow], get_Owner method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_Owner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_Owner


## -description



The <code>get_Owner</code> method retrieves the video window's parent window, if any.




## -parameters




### -param Owner

TBD




#### - pOwner [out]

Receives a handle to the window, as an <a href="https://msdn.microsoft.com/en-us/library/Dd390937(v=VS.85).aspx">OAHWND</a> type. If the video window has no parent, this parameter receives the value <b>NULL</b>.
          


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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>
 

 

