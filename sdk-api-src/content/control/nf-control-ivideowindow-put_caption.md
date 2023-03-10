---
UID: NF:control.IVideoWindow.put_Caption
title: IVideoWindow::put_Caption (control.h)
description: The put_Caption method sets the video window caption.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","put_Caption method","IVideoWindow.put_Caption","IVideoWindow::put_Caption","IVideoWindowput_Caption","control/IVideoWindow::put_Caption","dshow.ivideowindow_put_caption","put_Caption","put_Caption method [DirectShow]","put_Caption method [DirectShow]","IVideoWindow interface"]
old-location: dshow\ivideowindow_put_caption.htm
tech.root: dshow
ms.assetid: d16dca01-95ba-4573-b9c4-ab996dcf21e4
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],put_Caption method, IVideoWindow.put_Caption, IVideoWindow::put_Caption, IVideoWindowput_Caption, control/IVideoWindow::put_Caption, dshow.ivideowindow_put_caption, put_Caption, put_Caption method [DirectShow], put_Caption method [DirectShow],IVideoWindow interface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVideoWindow::put_Caption
 - control/IVideoWindow::put_Caption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.put_Caption
---

# IVideoWindow::put_Caption


## -description

The <code>put_Caption</code> method sets the video window caption.

## -parameters

### -param strCaption [in]

A <b>BSTR</b> that contains the caption.

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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>



<a href="/windows/desktop/api/control/nf-control-ivideowindow-get_caption">IVideoWindow::get_Caption</a>