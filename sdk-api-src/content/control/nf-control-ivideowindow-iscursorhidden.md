---
UID: NF:control.IVideoWindow.IsCursorHidden
title: IVideoWindow::IsCursorHidden (control.h)
description: The IsCursorHidden method queries whether the cursor is hidden.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","IsCursorHidden method","IVideoWindow.IsCursorHidden","IVideoWindow::IsCursorHidden","IVideoWindowIsCursorHidden","IsCursorHidden","IsCursorHidden method [DirectShow]","IsCursorHidden method [DirectShow]","IVideoWindow interface","control/IVideoWindow::IsCursorHidden","dshow.ivideowindow_iscursorhidden"]
old-location: dshow\ivideowindow_iscursorhidden.htm
tech.root: dshow
ms.assetid: 240040d8-433e-4398-a20a-66cc5a27bdae
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],IsCursorHidden method, IVideoWindow.IsCursorHidden, IVideoWindow::IsCursorHidden, IVideoWindowIsCursorHidden, IsCursorHidden, IsCursorHidden method [DirectShow], IsCursorHidden method [DirectShow],IVideoWindow interface, control/IVideoWindow::IsCursorHidden, dshow.ivideowindow_iscursorhidden
f1_keywords:
- control/IVideoWindow.IsCursorHidden
dev_langs:
- c++
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
- IVideoWindow.IsCursorHidden
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-hidecursor">IVideoWindow::HideCursor</a>
 

 

