---
UID: NF:textserv.ITextHost.TxGetSelectionBarWidth
title: ITextHost::TxGetSelectionBarWidth (textserv.h)
description: Returns the size of selection bar in HIMETRIC.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetSelectionBarWidth method","ITextHost.TxGetSelectionBarWidth","ITextHost::TxGetSelectionBarWidth","TxGetSelectionBarWidth","TxGetSelectionBarWidth method [Windows Controls]","TxGetSelectionBarWidth method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetSelectionBarWidth","_win32_ITextHost_TxGetSelectionBarWidth_cpp","controls.ITextHost_TxGetSelectionBarWidth","controls._win32_ITextHost_TxGetSelectionBarWidth","textserv/ITextHost::TxGetSelectionBarWidth"]
old-location: controls\ITextHost_TxGetSelectionBarWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetselectionbarwidth.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetSelectionBarWidth method, ITextHost.TxGetSelectionBarWidth, ITextHost::TxGetSelectionBarWidth, TxGetSelectionBarWidth, TxGetSelectionBarWidth method [Windows Controls], TxGetSelectionBarWidth method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetSelectionBarWidth, _win32_ITextHost_TxGetSelectionBarWidth_cpp, controls.ITextHost_TxGetSelectionBarWidth, controls._win32_ITextHost_TxGetSelectionBarWidth, textserv/ITextHost::TxGetSelectionBarWidth
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
 - ITextHost::TxGetSelectionBarWidth
 - textserv/ITextHost::TxGetSelectionBarWidth
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
 - ITextHost.TxGetSelectionBarWidth
---

# ITextHost::TxGetSelectionBarWidth


## -description

Returns the size of selection bar in HIMETRIC.

## -parameters

### -param lSelBarWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The width, in HIMETRIC (that is, where the units are .01 millimeter), of the selection bar.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>