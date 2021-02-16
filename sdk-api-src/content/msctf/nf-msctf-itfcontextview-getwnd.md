---
UID: NF:msctf.ITfContextView.GetWnd
title: ITfContextView::GetWnd (msctf.h)
description: The ITfContextView::GetWnd method returns the handle to a window that corresponds to the current document.
helpviewer_keywords: ["GetWnd","GetWnd method [Text Services Framework]","GetWnd method [Text Services Framework]","ITfContextView interface","ITfContextView interface [Text Services Framework]","GetWnd method","ITfContextView.GetWnd","ITfContextView::GetWnd","_tsf_itfcontextview_getwnd_ref","msctf/ITfContextView::GetWnd","tsf.itfcontextview_getwnd"]
old-location: tsf\itfcontextview_getwnd.htm
tech.root: TSF
ms.assetid: e805842d-4737-45be-8314-bd83d94da2d6
ms.date: 12/05/2018
ms.keywords: GetWnd, GetWnd method [Text Services Framework], GetWnd method [Text Services Framework],ITfContextView interface, ITfContextView interface [Text Services Framework],GetWnd method, ITfContextView.GetWnd, ITfContextView::GetWnd, _tsf_itfcontextview_getwnd_ref, msctf/ITfContextView::GetWnd, tsf.itfcontextview_getwnd
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextView::GetWnd
 - msctf/ITfContextView::GetWnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextView.GetWnd
---

# ITfContextView::GetWnd


## -description

The <b>ITfContextView::GetWnd</b> method returns the handle to a window that corresponds to the current document.

## -parameters

### -param phwnd [out]

Receives a pointer to the handle of the window that corresponds to the current document.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

A document might not have a corresponding window handle if the document is in memory but not displayed on the screen or if the document is a windowless control and the control does not have the window handle of the owner of the windowless controls. Callers cannot assume that the <i>phwnd</i> parameter will receive a non-<b>NULL</b> value even if the method is successful. Callers can also receive a <b>NULL</b> value for the <i>phwnd</i> parameter.

