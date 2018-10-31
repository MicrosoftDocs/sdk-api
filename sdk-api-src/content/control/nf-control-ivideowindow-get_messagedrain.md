---
UID: NF:control.IVideoWindow.get_MessageDrain
title: IVideoWindow::get_MessageDrain
author: windows-sdk-content
description: The get_MessageDrain method retrieves the window that receives mouse and keyboard messages from the video window, if any.
old-location: dshow\ivideowindow_get_messagedrain.htm
tech.root: DirectShow
ms.assetid: 9a1a3070-5b68-4dd2-bc10-97a8331cc262
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IVideoWindow interface [DirectShow],get_MessageDrain method, IVideoWindow.get_MessageDrain, IVideoWindow::get_MessageDrain, IVideoWindowget_MessageDrain, control/IVideoWindow::get_MessageDrain, dshow.ivideowindow_get_messagedrain, get_MessageDrain, get_MessageDrain method [DirectShow], get_MessageDrain method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.get_MessageDrain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::get_MessageDrain


## -description



The <code>get_MessageDrain</code> method retrieves the window that receives mouse and keyboard messages from the video window, if any.




## -parameters




### -param Drain [in]

Receives a handle to the window, as an <a href="https://msdn.microsoft.com/80194b19-9c24-48f5-aca6-6ab33bd88c90">OAHWND</a> type. If no message drain was set, this parameter receives the value <b>NULL</b>.
          


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



<a href="https://msdn.microsoft.com/aaf8624c-b3ea-4034-845a-6cd74c725c44">IVideoWindow::put_MessageDrain</a>
 

 

