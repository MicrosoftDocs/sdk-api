---
UID: NF:control.IVideoWindow.get_Caption
title: IVideoWindow::get_Caption (control.h)
description: The get_Caption method retrieves the video window caption.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","get_Caption method","IVideoWindow.get_Caption","IVideoWindow::get_Caption","IVideoWindowget_Caption","control/IVideoWindow::get_Caption","dshow.ivideowindow_get_caption","get_Caption","get_Caption method [DirectShow]","get_Caption method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_get_caption.htm
tech.root: dshow
ms.assetid: fbb42e55-1be1-4931-869b-9e8d4af5e6df
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],get_Caption method, IVideoWindow.get_Caption, IVideoWindow::get_Caption, IVideoWindowget_Caption, control/IVideoWindow::get_Caption, dshow.ivideowindow_get_caption, get_Caption, get_Caption method [DirectShow], get_Caption method [DirectShow],IVideoWindow interface
f1_keywords:
- control/IVideoWindow.get_Caption
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
- IVideoWindow.get_Caption
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoWindow::get_Caption


## -description



The <code>get_Caption</code> method retrieves the video window caption.




## -parameters




### -param strCaption [out]

Pointer to a <b>BSTR</b> that receives the caption.


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
 




## -remarks



The caller must free the returned string, using the <b>SysFreeString</b> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-ivideowindow-put_caption">IVideoWindow::put_Caption</a>
 

 

