---
UID: NF:control.IVideoWindow.HideCursor
title: IVideoWindow::HideCursor
author: windows-sdk-content
description: The HideCursor method shows or hides the cursor when the mouse is positioned over the video window.
old-location: dshow\ivideowindow_hidecursor.htm
tech.root: DirectShow
ms.assetid: c45da114-6711-427b-8533-4ed339a42ff4
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: HideCursor, HideCursor method [DirectShow], HideCursor method [DirectShow],IVideoWindow interface, IVideoWindow interface [DirectShow],HideCursor method, IVideoWindow.HideCursor, IVideoWindow::HideCursor, IVideoWindowHideCursor, OAFALSE, OATRUE, control/IVideoWindow::HideCursor, dshow.ivideowindow_hidecursor
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
 - IVideoWindow.HideCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVideoWindow::HideCursor


## -description



The <code>HideCursor</code> method shows or hides the cursor when the mouse is positioned over the video window.




## -parameters




### -param HideCursor [in]

Specifies whether to show or hide the cursor. Must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OATRUE"></a><a id="oatrue"></a><dl>
<dt><b>OATRUE</b></dt>
</dl>
</td>
<td width="60%">
Hide the cursor.

</td>
</tr>
<tr>
<td width="40%"><a id="OAFALSE"></a><a id="oafalse"></a><dl>
<dt><b>OAFALSE</b></dt>
</dl>
</td>
<td width="60%">
Show the cursor.

</td>
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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377276(v=VS.85).aspx">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd377308(v=VS.85).aspx">IVideoWindow::IsCursorHidden</a>
 

 

