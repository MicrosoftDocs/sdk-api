---
UID: NF:textserv.ITextHost.TxSetScrollPos
title: ITextHost::TxSetScrollPos (textserv.h)
description: Sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box. (ITextHost.TxSetScrollPos)
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxSetScrollPos method","ITextHost.TxSetScrollPos","ITextHost::TxSetScrollPos","TxSetScrollPos","TxSetScrollPos method [Windows Controls]","TxSetScrollPos method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxSetScrollPos","_win32_ITextHost_TxSetScrollPos_cpp","controls.ITextHost_TxSetScrollPos","controls._win32_ITextHost_TxSetScrollPos","textserv/ITextHost::TxSetScrollPos"]
old-location: controls\ITextHost_TxSetScrollPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsetscrollpos.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetScrollPos method, ITextHost.TxSetScrollPos, ITextHost::TxSetScrollPos, TxSetScrollPos, TxSetScrollPos method [Windows Controls], TxSetScrollPos method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetScrollPos, _win32_ITextHost_TxSetScrollPos_cpp, controls.ITextHost_TxSetScrollPos, controls._win32_ITextHost_TxSetScrollPos, textserv/ITextHost::TxSetScrollPos
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
 - ITextHost::TxSetScrollPos
 - textserv/ITextHost::TxSetScrollPos
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
 - ITextHost.TxSetScrollPos
---

# ITextHost::TxSetScrollPos


## -description

Sets the position of the scroll box (thumb) in the specified scroll bar and, if requested, redraws the scroll bar to reflect the new position of the scroll box.

## -parameters

### -param fnBar [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Scroll bar flag. If this is SB_HORZ, horizontal scrolling is done. By default, vertical scrolling is done.

### -param nPos [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

New position in scroll box. This must be within the range of scroll bar values set by <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txsetscrollrange">ITextHost::TxSetScrollRange</a>.

### -param fRedraw [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Redraw flag. If <b>TRUE</b>, the scroll bar is redrawn with the new position of the scroll box. If <b>FALSE</b>, the scroll bar is not redrawn.

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



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txsetscrollrange">TxSetScrollRange</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>
