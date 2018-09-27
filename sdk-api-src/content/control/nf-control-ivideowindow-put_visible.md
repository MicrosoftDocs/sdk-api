---
UID: NF:control.IVideoWindow.put_Visible
title: IVideoWindow::put_Visible
author: windows-sdk-content
description: The put_Visible method shows or hides the video window.
old-location: dshow\ivideowindow_put_visible.htm
tech.root: DirectShow
ms.assetid: ae789f07-4d50-488c-b57e-2b003a8cde3e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Visible method, IVideoWindow.put_Visible, IVideoWindow::put_Visible, IVideoWindowput_Visible, control/IVideoWindow::put_Visible, dshow.ivideowindow_put_visible, put_Visible, put_Visible method [DirectShow], put_Visible method [DirectShow],IVideoWindow interface
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
 - IVideoWindow.put_Visible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::put_Visible


## -description



The <code>put_Visible</code> method shows or hides the video window.




## -parameters




### -param Visible [in]

Specifies whether to show or hide the window. Must be one of the following values:
            

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE
                </td>
<td>Show the window.</td>
</tr>
<tr>
<td>OAFALSE
                </td>
<td>Hide the window.</td>
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



<a href="https://msdn.microsoft.com/b533398e-80f6-4f33-982b-93b8e0d705e9">IVideoWindow::get_Visible</a>
 

 

