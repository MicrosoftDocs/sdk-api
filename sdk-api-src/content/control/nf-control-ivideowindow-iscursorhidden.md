---
UID: NF:control.IVideoWindow.IsCursorHidden
title: IVideoWindow::IsCursorHidden
author: windows-sdk-content
description: The IsCursorHidden method queries whether the cursor is hidden.
old-location: dshow\ivideowindow_iscursorhidden.htm
old-project: DirectShow
ms.assetid: 240040d8-433e-4398-a20a-66cc5a27bdae
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVideoWindow interface [DirectShow],IsCursorHidden method, IVideoWindow.IsCursorHidden, IVideoWindow::IsCursorHidden, IVideoWindowIsCursorHidden, IsCursorHidden, IsCursorHidden method [DirectShow], IsCursorHidden method [DirectShow],IVideoWindow interface, control/IVideoWindow::IsCursorHidden, dshow.ivideowindow_iscursorhidden
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
 - IVideoWindow.IsCursorHidden
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IVideoWindow::IsCursorHidden


## -description



The <code>IsCursorHidden</code> method queries whether the cursor is hidden.




## -parameters




### -param CursorHidden [out]

Receives the value OATRUE if the cursor is hidden, or OAFALSE if the cursor is displayed.
          


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



<a href="https://msdn.microsoft.com/en-us/library/Dd377306(v=VS.85).aspx">IVideoWindow::HideCursor</a>
 

 

