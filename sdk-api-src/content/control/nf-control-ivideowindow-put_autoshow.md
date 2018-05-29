---
UID: NF:control.IVideoWindow.put_AutoShow
title: IVideoWindow::put_AutoShow
author: windows-sdk-content
description: The put_AutoShow method specifies whether the video renderer automatically shows the video window when it receives video data.
old-location: dshow\ivideowindow_put_autoshow.htm
old-project: DirectShow
ms.assetid: 7481a7e8-4b57-43cc-8304-b70616bbd532
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IVideoWindow interface [DirectShow],put_AutoShow method, IVideoWindow.put_AutoShow, IVideoWindow::put_AutoShow, IVideoWindowput_AutoShow, control/IVideoWindow::put_AutoShow, dshow.ivideowindow_put_autoshow, put_AutoShow, put_AutoShow method [DirectShow], put_AutoShow method [DirectShow],IVideoWindow interface
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
-	IVideoWindow.put_AutoShow
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::put_AutoShow


## -description



The <code>put_AutoShow</code> method specifies whether the video renderer automatically shows the video window when it receives video data.




## -parameters




### -param AutoShow [in]

Specifies whether the video renderer automatically shows the video window. Must be one of the following values:

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
<td>If the video renderer pauses or runs, it will automatically show the video window. (Default.)</td>
</tr>
<tr>
<td>
                  OAFALSE
                </td>
<td>The video renderer will not automatically show the video window.</td>
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
 




## -remarks



By default, when the filter graph changes state to paused or running, the video renderer shows the video window and moves it to the foreground. If the user closes the window, it will not automatically reappear.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/6f42e37d-af67-4f9e-8a02-d1f4154df391">IVideoWindow::get_AutoShow</a>
 

 

