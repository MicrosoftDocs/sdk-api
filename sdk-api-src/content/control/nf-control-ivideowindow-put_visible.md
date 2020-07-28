---
UID: NF:control.IVideoWindow.put_Visible
title: IVideoWindow::put_Visible (control.h)
description: The put_Visible method shows or hides the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_Visible method","IVideoWindow.put_Visible","IVideoWindow::put_Visible","IVideoWindowput_Visible","control/IVideoWindow::put_Visible","dshow.ivideowindow_put_visible","put_Visible","put_Visible method [DirectShow]","put_Visible method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_visible.htm
tech.root: dshow
ms.assetid: ae789f07-4d50-488c-b57e-2b003a8cde3e
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Visible method, IVideoWindow.put_Visible, IVideoWindow::put_Visible, IVideoWindowput_Visible, control/IVideoWindow::put_Visible, dshow.ivideowindow_put_visible, put_Visible, put_Visible method [DirectShow], put_Visible method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.put_Visible
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
- IVideoWindow.put_Visible
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-get_visible">IVideoWindow::get_Visible</a>
 

 

