---
UID: NF:textserv.ITextHost.TxShowCaret
title: ITextHost::TxShowCaret (textserv.h)
description: Shows or hides the caret at the caret position in the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxShowCaret method","ITextHost.TxShowCaret","ITextHost::TxShowCaret","TxShowCaret","TxShowCaret method [Windows Controls]","TxShowCaret method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxShowCaret","_win32_ITextHost_TxShowCaret_cpp","controls.ITextHost_TxShowCaret","controls._win32_ITextHost_TxShowCaret","textserv/ITextHost::TxShowCaret"]
old-location: controls\ITextHost_TxShowCaret.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txshowcaret.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxShowCaret method, ITextHost.TxShowCaret, ITextHost::TxShowCaret, TxShowCaret, TxShowCaret method [Windows Controls], TxShowCaret method [Windows Controls],ITextHost interface, _win32_ITextHost_TxShowCaret, _win32_ITextHost_TxShowCaret_cpp, controls.ITextHost_TxShowCaret, controls._win32_ITextHost_TxShowCaret, textserv/ITextHost::TxShowCaret
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
 - ITextHost::TxShowCaret
 - textserv/ITextHost::TxShowCaret
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
 - ITextHost.TxShowCaret
---

# ITextHost::TxShowCaret


## -description

Shows or hides the caret at the caret position in the text host window.

## -parameters

### -param fShow [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Flag. If <b>TRUE</b>, the caret is visible. If <b>FALSE</b>, the caret is hidden.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the method succeeds. 

Return <b>FALSE</b> if the method fails.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txcreatecaret">TxCreateCaret</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txsetcaretpos">TxSetCaretPos</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>