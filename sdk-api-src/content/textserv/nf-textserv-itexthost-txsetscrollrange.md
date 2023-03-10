---
UID: NF:textserv.ITextHost.TxSetScrollRange
title: ITextHost::TxSetScrollRange (textserv.h)
description: Sets the minimum and maximum position values for the specified scroll bar in the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxSetScrollRange method","ITextHost.TxSetScrollRange","ITextHost::TxSetScrollRange","TxSetScrollRange","TxSetScrollRange method [Windows Controls]","TxSetScrollRange method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxSetScrollRange","_win32_ITextHost_TxSetScrollRange_cpp","controls.ITextHost_TxSetScrollRange","controls._win32_ITextHost_TxSetScrollRange","textserv/ITextHost::TxSetScrollRange"]
old-location: controls\ITextHost_TxSetScrollRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsetscrollrange.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetScrollRange method, ITextHost.TxSetScrollRange, ITextHost::TxSetScrollRange, TxSetScrollRange, TxSetScrollRange method [Windows Controls], TxSetScrollRange method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetScrollRange, _win32_ITextHost_TxSetScrollRange_cpp, controls.ITextHost_TxSetScrollRange, controls._win32_ITextHost_TxSetScrollRange, textserv/ITextHost::TxSetScrollRange
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
 - ITextHost::TxSetScrollRange
 - textserv/ITextHost::TxSetScrollRange
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
 - ITextHost.TxSetScrollRange
---

# ITextHost::TxSetScrollRange


## -description

Sets the minimum and maximum position values for the specified scroll bar in the text host window.

## -parameters

### -param fnBar [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Scroll bar flag. If this is SB_HORZ, horizontal scrolling is done. By default, vertical scrolling is done.

### -param nMinPos [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Minimum scrolling position.

### -param nMaxPos [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Maximum scrolling position.

### -param fRedraw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Redraw flag. If <b>TRUE</b>, the scroll bar is redrawn to reflect the changes. If <b>FALSE</b>, the scroll bar is not redrawn.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Return <b>TRUE</b> if the arrows are enabled or disabled as specified. 

Return <b>FALSE</b> if the arrows are already in the requested state or an error occurs.

## -remarks

This method is only valid when the control is in-place active; calls while the control is inactive may fail.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>