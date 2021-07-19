---
UID: NF:textserv.ITextHost2.TxIsDoubleClickPending
title: ITextHost2::TxIsDoubleClickPending (textserv.h)
description: Discovers whether the message queue contains a WM_LBUTTONDBLCLK message that is pending for the text host window.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxIsDoubleClickPending method","ITextHost2.TxIsDoubleClickPending","ITextHost2::TxIsDoubleClickPending","TxIsDoubleClickPending","TxIsDoubleClickPending method [Windows Controls]","TxIsDoubleClickPending method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txisdoubleclickpending","textserv/ITextHost2::TxIsDoubleClickPending"]
old-location: controls\itexthost2_txisdoubleclickpending.htm
tech.root: Controls
ms.assetid: 24051A4F-70CD-4147-B623-BC818F3F9AF2
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxIsDoubleClickPending method, ITextHost2.TxIsDoubleClickPending, ITextHost2::TxIsDoubleClickPending, TxIsDoubleClickPending, TxIsDoubleClickPending method [Windows Controls], TxIsDoubleClickPending method [Windows Controls],ITextHost2 interface, controls.itexthost2_txisdoubleclickpending, textserv/ITextHost2::TxIsDoubleClickPending
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextHost2::TxIsDoubleClickPending
 - textserv/ITextHost2::TxIsDoubleClickPending
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
 - ITextHost2.TxIsDoubleClickPending
---

# ITextHost2::TxIsDoubleClickPending


## -description

Discovers whether the message queue contains a <a href="/windows/desktop/inputdev/wm-lbuttondblclk">WM_LBUTTONDBLCLK</a>  message that is pending for the text host window.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if a <a href="/windows/desktop/inputdev/wm-lbuttondblclk">WM_LBUTTONDBLCLK</a> message is pending, or <b>FALSE</b> if not.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>
