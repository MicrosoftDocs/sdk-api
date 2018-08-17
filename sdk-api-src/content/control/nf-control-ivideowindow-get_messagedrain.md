---
UID: NF:control.IVideoWindow.get_MessageDrain
title: IVideoWindow::get_MessageDrain
author: windows-sdk-content
description: The get_MessageDrain method retrieves the window that receives mouse and keyboard messages from the video window, if any.
old-location: dshow\ivideowindow_get_messagedrain.htm
old-project: DirectShow
ms.assetid: 9a1a3070-5b68-4dd2-bc10-97a8331cc262
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVideoWindow interface [DirectShow],get_MessageDrain method, IVideoWindow.get_MessageDrain, IVideoWindow::get_MessageDrain, IVideoWindowget_MessageDrain, control/IVideoWindow::get_MessageDrain, dshow.ivideowindow_get_messagedrain, get_MessageDrain, get_MessageDrain method [DirectShow], get_MessageDrain method [DirectShow],IVideoWindow interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
 - IVideoWindow.get_MessageDrain
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::get_MessageDrain


## -description



The <code>get_MessageDrain</code> method retrieves the window that receives mouse and keyboard messages from the video window, if any.




## -parameters




### -param Drain [in]

Receives a handle to the window, as an <a href="https://msdn.microsoft.com/en-us/library/Dd390937(v=VS.85).aspx">OAHWND</a> type. If no message drain was set, this parameter receives the value <b>NULL</b>.
          


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



<a href="https://msdn.microsoft.com/en-us/library/Dd377323(v=VS.85).aspx">IVideoWindow::put_MessageDrain</a>
 

 

