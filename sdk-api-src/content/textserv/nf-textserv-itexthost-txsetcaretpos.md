---
UID: NF:textserv.ITextHost.TxSetCaretPos
title: ITextHost::TxSetCaretPos (textserv.h)
description: Moves the caret position to the specified coordinates in the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxSetCaretPos method","ITextHost.TxSetCaretPos","ITextHost::TxSetCaretPos","TxSetCaretPos","TxSetCaretPos method [Windows Controls]","TxSetCaretPos method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxSetCaretPos","_win32_ITextHost_TxSetCaretPos_cpp","controls.ITextHost_TxSetCaretPos","controls._win32_ITextHost_TxSetCaretPos","textserv/ITextHost::TxSetCaretPos"]
old-location: controls\ITextHost_TxSetCaretPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxsetcaretpos.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetCaretPos method, ITextHost.TxSetCaretPos, ITextHost::TxSetCaretPos, TxSetCaretPos, TxSetCaretPos method [Windows Controls], TxSetCaretPos method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetCaretPos, _win32_ITextHost_TxSetCaretPos_cpp, controls.ITextHost_TxSetCaretPos, controls._win32_ITextHost_TxSetCaretPos, textserv/ITextHost::TxSetCaretPos
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
 - ITextHost::TxSetCaretPos
 - textserv/ITextHost::TxSetCaretPos
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
 - ITextHost.TxSetCaretPos
---

# ITextHost::TxSetCaretPos


## -description

Moves the caret position to the specified coordinates in the text host window.

## -parameters

### -param x [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Horizontal position (in client coordinates).

### -param y [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Vertical position (in client coordinates).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>