---
UID: NF:textserv.ITextHost.TxSetCursor
title: ITextHost::TxSetCursor (textserv.h)
description: Establishes a new cursor shape (I-beam) in the text host's window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxSetCursor method","ITextHost.TxSetCursor","ITextHost::TxSetCursor","TxSetCursor","TxSetCursor method [Windows Controls]","TxSetCursor method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxSetCursor","_win32_ITextHost_TxSetCursor_cpp","controls.ITextHost_TxSetCursor","controls._win32_ITextHost_TxSetCursor","textserv/ITextHost::TxSetCursor"]
old-location: controls\ITextHost_TxSetCursor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsetcursor.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxSetCursor method, ITextHost.TxSetCursor, ITextHost::TxSetCursor, TxSetCursor, TxSetCursor method [Windows Controls], TxSetCursor method [Windows Controls],ITextHost interface, _win32_ITextHost_TxSetCursor, _win32_ITextHost_TxSetCursor_cpp, controls.ITextHost_TxSetCursor, controls._win32_ITextHost_TxSetCursor, textserv/ITextHost::TxSetCursor
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
 - ITextHost::TxSetCursor
 - textserv/ITextHost::TxSetCursor
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
 - ITextHost.TxSetCursor
---

# ITextHost::TxSetCursor


## -description

Establishes a new cursor shape (I-beam) in the text host's window.

## -parameters

### -param hcur [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HCURSOR</a></b>

Handle to the cursor.

### -param fText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>TRUE</b>, indicates the caller is trying to set the text cursor. See the Remarks section for more information.

## -remarks

This method may be called at any time, whether the control is active or inactive.

<b>TxSetCursor</b> should be called by the text services object to set the mouse cursor. If the <i>fText</i> parameter is <b>TRUE</b>, the text services object is trying to set the text cursor (the cursor appears as an I-beam when it is over text that is not selected). In this case, the host can set it to whatever the control MousePointer property is. This is required for Microsoft Visual Basic compatibility since, through the MousePointer property, the Visual Basic programmer has control over the shape of the mouse cursor.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>