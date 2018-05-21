---
UID: NF:control.IVideoWindow.IsCursorHidden
title: IVideoWindow::IsCursorHidden
author: windows-driver-content
description: The IsCursorHidden method queries whether the cursor is hidden.
old-location: dshow\ivideowindow_iscursorhidden.htm
old-project: DirectShow
ms.assetid: 240040d8-433e-4398-a20a-66cc5a27bdae
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IVideoWindow interface [DirectShow],IsCursorHidden method, IVideoWindow.IsCursorHidden, IVideoWindow::IsCursorHidden, IVideoWindowIsCursorHidden, IsCursorHidden, IsCursorHidden method [DirectShow], IsCursorHidden method [DirectShow],IVideoWindow interface, control/IVideoWindow::IsCursorHidden, dshow.ivideowindow_iscursorhidden
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
-	IVideoWindow.IsCursorHidden
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8e931c15-bd1d-409e-ada1-97fe49125fe7">IVideoWindow Interface</a>



<a href="https://msdn.microsoft.com/c45da114-6711-427b-8533-4ed339a42ff4">IVideoWindow::HideCursor</a>
 

 

