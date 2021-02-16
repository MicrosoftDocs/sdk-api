---
UID: NF:textserv.ITextServices.TxGetBaseLinePos
title: ITextServices::TxGetBaseLinePos (textserv.h)
description: Gets the base line position of the first visible line, in pixels, relative to the text services client rectangle. This permits aligning controls on their base lines.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxGetBaseLinePos method","ITextServices.TxGetBaseLinePos","ITextServices::TxGetBaseLinePos","TxGetBaseLinePos","TxGetBaseLinePos method [Windows Controls]","TxGetBaseLinePos method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxGetBaseLinePos","_win32_ITextServices_TxGetBaseLinePos_cpp","controls.ITextServices_TxGetBaseLinePos","controls._win32_ITextServices_TxGetBaseLinePos","textserv/ITextServices::TxGetBaseLinePos"]
old-location: controls\ITextServices_TxGetBaseLinePos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetbaselinepos.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetBaseLinePos method, ITextServices.TxGetBaseLinePos, ITextServices::TxGetBaseLinePos, TxGetBaseLinePos, TxGetBaseLinePos method [Windows Controls], TxGetBaseLinePos method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetBaseLinePos, _win32_ITextServices_TxGetBaseLinePos_cpp, controls.ITextServices_TxGetBaseLinePos, controls._win32_ITextServices_TxGetBaseLinePos, textserv/ITextServices::TxGetBaseLinePos
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextServices::TxGetBaseLinePos
 - textserv/ITextServices::TxGetBaseLinePos
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices.TxGetBaseLinePos
---

# ITextServices::TxGetBaseLinePos


## -description

Gets the base line position of the first visible line, in pixels, relative to the text services client rectangle. This permits aligning controls on their base lines.

## -parameters

#### - pBaseLinePos

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The base line position of the first visible line.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is the following <b>HRESULT</b> code. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>