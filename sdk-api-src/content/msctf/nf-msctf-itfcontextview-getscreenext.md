---
UID: NF:msctf.ITfContextView.GetScreenExt
title: ITfContextView::GetScreenExt (msctf.h)
description: The ITfContextView::GetScreenExt method returns the bounding box, in screen coordinates, of the document display.
helpviewer_keywords: ["GetScreenExt","GetScreenExt method [Text Services Framework]","GetScreenExt method [Text Services Framework]","ITfContextView interface","ITfContextView interface [Text Services Framework]","GetScreenExt method","ITfContextView.GetScreenExt","ITfContextView::GetScreenExt","_tsf_itfcontextview_getscreenext_ref","msctf/ITfContextView::GetScreenExt","tsf.itfcontextview_getscreenext"]
old-location: tsf\itfcontextview_getscreenext.htm
tech.root: TSF
ms.assetid: 86dde611-4c46-418c-aa89-728081a28943
ms.date: 12/05/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITfContextView interface, ITfContextView interface [Text Services Framework],GetScreenExt method, ITfContextView.GetScreenExt, ITfContextView::GetScreenExt, _tsf_itfcontextview_getscreenext_ref, msctf/ITfContextView::GetScreenExt, tsf.itfcontextview_getscreenext
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
 - ITfContextView::GetScreenExt
 - msctf/ITfContextView::GetScreenExt
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
 - ITfContextView.GetScreenExt
---

# ITfContextView::GetScreenExt


## -description

The <b>ITfContextView::GetScreenExt</b> method returns the bounding box, in screen coordinates, of the document display.

## -parameters

### -param prc [out]

Receives the bounding box, in screen coordinates, of the display surface.

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

The <i>prc</i> parameter is cleared to {0,0,0,0} if the document is not currently displayed.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getscreenext">ITextStoreACP::GetScreenExt
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getscreenext">ITfContextOwner::GetScreenExt
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView</a>



<a href="/windows/desktop/TSF/tsviewcookie">TsViewCookie
      </a>