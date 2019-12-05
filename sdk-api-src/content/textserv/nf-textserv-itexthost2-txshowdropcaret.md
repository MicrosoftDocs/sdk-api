---
UID: NF:textserv.ITextHost2.TxShowDropCaret
title: ITextHost2::TxShowDropCaret (textserv.h)
description: Shows or hides the caret during the drop portion of a drag-and-drop operation (Direct2D only).
old-location: controls\itexthost2_txshowdropcaret.htm
tech.root: Controls
ms.assetid: D7FAD45E-3467-4F07-A0D9-3131E48C314B
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxShowDropCaret method, ITextHost2.TxShowDropCaret, ITextHost2::TxShowDropCaret, TxShowDropCaret, TxShowDropCaret method [Windows Controls], TxShowDropCaret method [Windows Controls],ITextHost2 interface, controls.itexthost2_txshowdropcaret, textserv/ITextHost2::TxShowDropCaret
ms.topic: method
f1_keywords:
- textserv/ITextHost2.TxShowDropCaret
dev_langs:
- c++
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msftedit.dll
api_name:
- ITextHost2.TxShowDropCaret
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost2::TxShowDropCaret


## -description


Shows or hides the  caret during the drop portion of a drag-and-drop operation (Direct2D only).


## -parameters




### -param fShow

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Show or hide flag. <b>TRUE</b> shows the drop caret, and <b>FALSE</b> hides it.


### -param hdc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HDC</a></b>

The HDC.


### -param prc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">LPCRECT</a></b>

The drop caret rectangle.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>
 

 

